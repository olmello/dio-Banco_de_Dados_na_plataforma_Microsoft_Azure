# Laboratório Prático: Instância Gerenciada de SQL do Azure

Pre-requisitos:
  - Ter conta ativa no azure
  - Permissões adequadas na assinatura

Cuidados
  - Cuidado ao criar o recurso pois pode gerar custos financeiros acima do esperado ou de remover o serviço em caso de gratuidade e o poerído de testes expirar.


## Passo a Passo da Configuração

1. Criando a Instância Gerenciada
1.1 - Configurações Básicas
Acesso ao serviço: No Portal do Azure, busquei por "Instância Gerenciada de SQL do Azure".

** Oferta gratuita: Aceitei a oferta promocional de 720 horas de vCore e 64GB de armazenamento - ideal para testes sem custos. **

Configurações principais:

Assinatura e Grupo de Recursos: Utilizei uma existente criada para tutoriais
Nome da instância: Padrão gerado automaticamente (free-sql-mi05590099)
Região: US West 2 (padrão sugerido)
Autenticação: Microsoft Entra ID selecionado (mais seguro que autenticação SQL padrão)
Imagem sugerida: Tela da guia "Básico" com as configurações preenchidas

1.2 - Configurações de Rede
Rede virtual: Criei uma nova rede virtual com sub-rede padrão

Configuração automática: O Azure automaticamente aplica as configurações necessárias para a Instância Gerenciada
Tipo de conexão: Mantido como padrão
Ponto de extremidade público: Habilitado com acesso da Internet (para facilitar testes iniciais, mas em produção recomenda-se configuração mais restritiva)
Importante: AO habilitar o ponto de extremidade público exige configuração cuidadosa de regras de firewall para manter a segurança.

1.3 - Configurações de Segurança
Microsoft Defender para SQL: Ativei o período de avaliação gratuita de 30 dias

Esta ferramenta oferece:
Avaliação de vulnerabilidades
Detecção de ameaças avançada
Recomendações de proteção de dados

1.4 - Configurações Adicionais

Ordenação: SQL_Latin1_General_CP1_CI_AS (compatível com muitas aplicações em inglês)
Fuso horário: UTC (padronizado para serviços globais)
Replicação geográfica: Desabilitada (para manter o custo zero)
Política de atualização: SQL Server 2022 (garantindo compatibilidade específica)

1.5 - Rótulos (Tags)
Decisão: Não adicionei tags nesta configuração de teste

Cenários de uso real:
  ambiente: desenvolvimento
  projeto: laboratorio-dio
  responsavel: Luis
  custo-centro: TI

1.6 - Revisão Final
Verificação: Revisei todas as configurações na guia "Revisar + criar"
Decisão estratégica: Cancelei a criação para preservar as horas gratuitas para uso futuro

AO realizar este laboratório, aprendi na prática:

✅ Configuração de serviços PaaS no Azure

✅ Tomada de decisões arquiteturais (segurança, rede, custos)

✅ Documentação técnica de processos

✅ Utilização do GitHub para portfólio técnico




