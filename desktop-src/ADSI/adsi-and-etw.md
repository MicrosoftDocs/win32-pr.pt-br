---
title: Rastreamento de eventos no ADSI
description: Windows o Server 2008 e o Windows Vista apresentam rastreamento de eventos em Interfaces de serviço Active Directory (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- ADSI de rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ff881a408e2f6d7a6b661e7556c8d39366f726
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469193"
---
# <a name="event-tracing-in-adsi"></a>Rastreamento de eventos no ADSI

Windows o Server 2008 e o Windows Vista apresentam [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) em [Interfaces de serviço Active Directory](active-directory-service-interfaces-adsi.md) (ADSI). Determinadas áreas do provedor de LDAP ADSI têm uma implementação subjacente que é complexa ou que envolve uma sequência de etapas que dificulta o diagnóstico de problemas. Para ajudar os desenvolvedores de aplicativos a solucionar problemas, o rastreamento de eventos foi adicionado às seguintes áreas:

## <a name="schema-parsing-and-downloading"></a>Análise e download de esquema

A interface IADs na ADSI requer que o esquema LDAP seja armazenado em cache no cliente para que os atributos possam ser empacotados corretamente (conforme descrito no [modelo de esquema ADSI](adsi-schema-model.md)). Para fazer isso, a ADSI carrega o esquema para cada processo (e para cada servidor/domínio LDAP) na memória a partir de um arquivo de esquema (. SCH) que é salvo no disco local ou baixando-o do servidor LDAP. Processos diferentes na mesma máquina cliente usam o esquema em cache em disco se ele estiver disponível e aplicável.

Se o esquema não puder ser obtido do disco ou do servidor, a ADSI usará um esquema padrão codificado. Quando isso ocorre, os atributos que não fazem parte desse esquema padrão não podem ser empacotados e a ADSI retorna um erro ao recuperar esses atributos. Vários fatores podem fazer com que isso aconteça, incluindo problemas na análise do esquema e privilégios insuficientes para baixar o esquema. Geralmente, é difícil determinar por que um determinado esquema padrão está sendo usado. Usar o rastreamento de eventos nessa área ajudará a diagnosticar o problema mais rapidamente e corrigi-lo.

## <a name="changing-and-setting-the-password"></a>Alterando e definindo a senha

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) e [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) empregam mais de um mecanismo para executar a operação solicitada com base na configuração disponível (conforme descrito em [definindo e alterando senhas de usuário com o provedor LDAP](setting-user-passwords-for-ldap-providers.md)). Quando **ChangePassword** e **SetPassword** falham, pode ser difícil determinar exatamente o porquê, e o rastreamento de eventos ajudará a solucionar problemas com esses métodos.

## <a name="adsi-bind-cache"></a>Cache de associação ADSI

O ADSI tenta, internamente, reutilizar conexões LDAP sempre que possível (consulte [Caching de conexão](connection-caching.md)). Ao solucionar problemas, é útil rastrear se uma nova conexão foi aberta para comunicação com o servidor ou se uma conexão existente foi usada. Também pode ser útil rastrear o ciclo de vida do cache de conexão (às vezes chamado de cache de associação) e sua criação ou fechamento e se uma indicação de conexão ocorreu. No caso de uma [ligação sem servidor](/windows/desktop/AD/serverless-binding-and-rootdse), a ADSI chama o localizador de DC para selecionar um servidor para o domínio do contexto do usuário. Em seguida, o ADSI mantém um cache do mapeamento do servidor de domínio para conexões subsequentes. O rastreamento de eventos ajuda a rastrear a seleção do controlador de domínio e, portanto, é útil para solucionar problemas relacionados à conexão.

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>Habilitando o rastreamento e iniciando uma sessão de rastreamento

Para ativar o rastreamento ADSI, crie a seguinte chave do registro:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** de \\  \\ **rastreamento** ADSI \\ **_ProcessName_**

*ProcessName* é o nome completo do processo que você deseja rastrear, incluindo sua extensão (por exemplo, "Svchost.exe"). Além disso, você pode inserir um valor opcional do tipo **DWORD** chamado PID nesta chave. É altamente recomendável que você defina esse valor e, portanto, rastreie apenas um processo específico. Caso contrário, todas as instâncias do aplicativo especificado por *ProcessName* serão rastreadas.

Em seguida, execute o seguinte comando:

**tracelog.exe-Start** *SessionName* **- \#** GUID do _provedor \__ **de GUID-f** *filename* **-Flag** *sinalizadores* **de nível de**  arquivo

*SessionName* é simplesmente um identificador arbitrário que é usado para rotular a sessão de rastreamento (você precisará se referir a esse nome de sessão posteriormente ao parar a sessão de rastreamento). O GUID do provedor de controle ADSI é "7288c9f8-D63C-4932-a345-89d6b060174d". *filename* especifica o arquivo de log no qual os eventos serão gravados. *sinalizadores* deve ser um dos seguintes valores:



|         Sinalizador                        |         Valor              |
|---------------------------------|-----------------------|
| **esquema de depuração \_**<br/>    | 0x00000001<br/> |
| **Depurar \_ CHANGEPWD**<br/> | 0x00000002<br/> |
| **Depurar \_ SETPWD**<br/>    | 0x00000004<br/> |
| **Depurar \_ BINDCACHE**<br/> | 0x00000008<br/> |



 

Esses sinalizadores determinam quais métodos [ADSI](active-directory-service-interfaces-adsi.md) serão rastreados, de acordo com a tabela a seguir:




| | | <strong>DEBUG_SCHEMA</strong><br /> | <ul><li>LdapGetSchema</li><li>GetSchemaInfoTime</li><li>LdapReadSchemaInfoFromServer</li><li>ProcessSchemaInfo</li><li>HelperReadLdapSchemaInfo</li><li>ProcessClassInfoArray</li><li>ReadSchemaInfoFromRegistry</li><li>StoreSchemaInfoFromRegistry</li><li>AttributeTypeDescription</li><li>ObjectClassDescription</li><li>DITContentRuleDescription</li><li>Directorystring</li><li>DirectoryStrings</li><li>DITContentRuleDescription</li></ul><br /> | | <strong>DEBUG_CHANGEPWD</strong><br /> | <ul><li>CADsUser:: ChangePassword</li></ul><br /> | | <strong>DEBUG_SETPWD</strong><br /> | <ul><li>CADsUser:: SetPassword</li></ul><br /> | | <strong>DEBUG_BINDCACHE</strong><br /> | <ul><li>GetServerBasedObject</li><li>GetServerLessBasedObject</li><li>GetGCDomainName</li><li>GetDefaultDomainName</li><li>GetUserDomainFlatName</li><li>BindCacheLookup</li><li>EquivalentPortNumbers</li><li>CanCredentialsBeReused</li><li>BindCacheAdd</li><li>BindCacheAddRef</li><li>AddReferralLink</li><li>CommonRemoveEntry</li><li>BindCacheDerefHelper</li><li>NotifyNewConnection</li><li>QueryForConnection</li><li>LdapOpenBindWithCredentials</li><li>LdapOpenBindWithDefaultCredentials</li></ul><br /> | 




 

Você pode combinar sinalizadores combinando os bits apropriados no argumento *sinalizadores* . Por exemplo, para especificar o **\_ esquema de depuração** e Depurar sinalizadores de **\_ BINDCACHE** , o valor de *sinalizadores* apropriado seria 0x00000009.

Por fim, o sinalizador *traceLevel* deve ser um dos seguintes valores:



|      Sinalizador                                    |       Valor                |
|------------------------------------------|-----------------------|
| **\_erro no nível de rastreamento \_**<br/>       | 0x00000002<br/> |
| **\_informações de nível de rastreamento \_**<br/> | 0x00000004<br/> |



 

**Rastrear \_ \_As informações de nível** fazem com que o processo de rastreamento Registre todos os eventos, enquanto que o **\_ \_ erro no nível de rastreamento** faz com que o processo de rastreamento grave apenas eventos de erro.

Para encerrar o rastreamento, execute o seguinte comando:

**tracelog.exe-parar** *SessionName*

No exemplo anterior, *SessionName* é o mesmo nome que aquele fornecido com o comando que iniciou a seção de rastreamento.

## <a name="remarks"></a>Comentários

É mais eficaz rastrear apenas processos específicos especificando um PID específico do que rastrear todos os processos em um computador. Se você precisar rastrear vários aplicativos no mesmo computador, poderá haver um impacto no desempenho; há uma saída substancial de depuração nas seções orientadas ao desempenho do código. Além disso, os administradores devem ter cuidado para definir corretamente as permissões dos arquivos de log ao rastrear vários processos; caso contrário, qualquer usuário poderá ler os logs de rastreamento e outros usuários poderão rastrear processos que contêm informações seguras.

Por exemplo, presume-se que o administrador configura o rastreamento para um aplicativo "Test.exe" e não especifica um PID no Registro para rastrear várias instâncias do processo. Agora, outro usuário deseja rastrear o aplicativo "Secure.exe". Se os arquivos de log de rastreamento não estão restritos corretamente, tudo o que o usuário precisa fazer é renomear "Secure.exe" como "Test.exe" e ele será rastreado. Em geral, é melhor rastrear apenas processos específicos durante a solução de problemas e remover a chave do Registro de rastreamento assim que a solução de problemas for feita.

Como a habilitação do Rastreamento de Eventos produzirá arquivos de log extras, os administradores devem monitorar cuidadosamente os tamanhos dos arquivos de log; a falta de espaço em disco no computador local pode causar uma negação de serviço.

## <a name="example-scenarios"></a>Cenários de Exemplo

Cenário 1: o administrador vê um erro inesperado em um aplicativo que define senhas para contas de usuário, portanto, ele seguiria as etapas a seguir para corrigir o problema usando o Rastreamento de Eventos.

1.  Escrever um script que reproduz o problema e criar a chave do Registro

    **HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**

2.  Inicie uma sessão de rastreamento, definindo *traceFlags* como 0x2 (**DEBUG \_ CHANGEPASSWD**) e *traceLevel* como 0x4 (**TRACE LEVEL \_ \_ INFORMATION**), usando o seguinte comando:

    **tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**

3.  Execute cscript.exe com o script de teste para reproduzir o problema e, em seguida, encerrar a sessão de rastreamento:

    **tracelog.exe -stop scripttrace**

4.  Excluir a chave do Registro

    **HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**

5.  Execute a ferramenta ETW Tracerpt.exe para analisar as informações de rastreamento do log:

    **tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**

Cenário 2: o administrador deseja rastrear as operações de análise e download de esquema em um aplicativo [ASP](https://msdn.microsoft.com/asp.net/default.aspx) chamado w3wp.exe que já está em execução. Para fazer isso, o administrador seguiria as seguintes etapas:

1.  Criar a chave do Registro

    **HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**

    e dentro dessa chave, crie um valor do tipo DWORD chamado PID e de definido como a ID de processo da instância do w3wp.exe que está sendo executado no computador local.

2.  Em seguida, eles criam uma sessão de rastreamento, definindo *traceFlags* como 0x1 (**DEBUG \_ SCHEMA**) e *traceLevel* como 0x4 (**TRACE LEVEL \_ \_ INFORMATION**):

    **tracelog.exe -start w3wptrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ w3wp.etl -flag 0x1 -level 0x4**

3.  Reproduza a operação que precisa de solução de problemas.
4.  Encerrar a sessão de rastreamento:

    **tracelog.exe -stop w3wptrace**

5.  Exclua a chave do Registro **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**.
6.  Execute a ferramenta ETW tracerpt.exe para analisar as informações de rastreamento do log:

    **tracerpt.exe . \\ w3wp.etl -o -report**

 

