 ## PROJETO AMIGO SECRETO 

 # ESTRUTURA DO PROJETO 
 ### Painel administrativo
 - Cadastrar Eventos
 - Cadastrar Grupos
 - Cadastrar Pessoas 
 

 ### Site 
 - Acessar tela do evento
 - Sorteio acontece na hora do CADASTRO, não na hora da indentificação.
 - No banco de dados, não podemos identificar quem tirou quem.
 - Painel adminstrativo deve ter uma senha unica


 ## Planejamento banco de dados  

 - EVENTOS
 - GRUPOS
 - PESSOAS 

### events
- id INT PK AUTO_INCREMENT
- status BOOLEAN default=false
- title STRING 
- description
- grouped BOOLEAN default=false

### eventGroups

- id INT PK AUTO_INCREMENT 
- id_event INT   
- name STRING
-  

eventPeople
- id INT PK AUTO_INCREMENT
- id_event INT(RELACIONANDO a events.id )
- id_group INT (RELACIONANDO a events.id)
- name STRING 
- cpf STRING  
- matched STRING default=""


## PLANEJAMENTO DE ROTAS 

- GET  /admin/events  -  LISTAR EVENTS
- GET  /admin/events/:id - LISTA UNICO EVENTO 
- POST /admin/events -  CRIAR UM EVENTO NOVO 
- PUT  /admin/events/:id ALTERANDO UM EVENTO
- DELETE /admin/events/:id DELETANDO UM EVENTO



- GET  /admin/events/:id_event/groups 
- GET  /admin/events/:id_event/groups/:id 
- POST /admin/events/:id_event/groups  
- PUT  /admin/events/:id_event/groups/:id  
- DELETE /admin/events/:id_event/groups/:id


- GET  /admin/events/:id_event/groups/people
- GET  /admin/events/:id_event/groups/people/:id 
- POST /admin/events/:id_event/groups/people  
- PUT  /admin/events/:id_event/groups/people/:id  
- DELETE /admin/events/:id_event/groups/people:id



- GET  /events/:id
- GET  /events/:id_event/person/:cpf










  




