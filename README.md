comando criação de usuário ADMIN: 
py manage.py shell

código: 
from ipe_roxo.models import CustomUser


admin_normal = CustomUser.objects.create_user(
    username='admin1',
    email='adminsite@exemplo.com',
    password='SenhaForte123!',
    tipo='ADMIN',
    ativo=True,
)


admin_normal.is_staff = False
admin_normal.is_superuser = False 
admin_normal.save()

em seguida: exit()

executar as migrações do banco: python manage.py makemigrations e python manage.py migrate   
