---
title: controle de acesso (plataforma de filtragem de Windows)
description: na WFP (plataforma de filtragem de Windows), o serviço BFE (mecanismo de filtragem Base) implementa o modelo de controle de acesso de Windows padrão com base em tokens de acesso e descritores de segurança.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad8d1cc292358b156a8853a8a141426fda638d64474d1413747e2ebdb59d7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901087"
---
# <a name="access-control-windows-filtering-platform"></a>controle de acesso (plataforma de filtragem de Windows)

na WFP (plataforma de filtragem de Windows), o serviço BFE (mecanismo de filtragem Base) implementa o [modelo de controle de acesso de Windows](/windows/desktop/SecAuthZ/access-control-model) padrão com base em tokens de acesso e descritores de segurança.

## <a name="access-control-model"></a>Modelo de controle de acesso

Descritores de segurança podem ser especificados ao adicionar novos objetos WFP, como filtros e subcamadas. Descritores de segurança são gerenciados usando as funções de gerenciamento de WFP **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0**, em que * *\** _ significa o nome do objeto WFP. essas funções são semanticamente idênticas às funções Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

> [!Note]  
> As funções **Fwpm \* SetSecurityInfo0** não podem ser chamadas de dentro de uma transação explícita.

 

> [!Note]  
> As funções **Fwpm \* SetSecurityInfo0** só podem ser chamadas de dentro de uma sessão dinâmica se estiverem sendo usadas para gerenciar um objeto dinâmico criado dentro da mesma sessão.

 

O descritor de segurança padrão para o mecanismo de filtro (o objeto do mecanismo raiz no diagrama abaixo) é o seguinte.

-   Conceda direitos de acesso **genéricos a \_ todos** (GA) ao grupo interno de administradores.
-   Conceda direitos de **acesso genérico de gravação \_** (GR) generic **\_ Write** (GW) genérico de **\_ execução** (GX) a operadores de configuração de rede.
-   conceda direitos de acesso **GRGWGX** aos seguintes ssids (identificadores de segurança de serviço): MpsSvc (Windows Firewall), NapAgent (agente de proteção de acesso à rede), PolicyAgent (agente de diretiva IPsec), rpcss (chamada de procedimento remoto) e WdiServiceHost (Host do serviço de diagnóstico).
-   Grant **FWPM \_ ACTRL \_ Open** e **FWPM \_ ACTRL \_ classificar** para todos. (Estes são direitos de acesso específicos da WFP, descritos na tabela abaixo.)

Os descritores de segurança padrão restantes são derivados por meio de herança.

Há algumas verificações de acesso, como para **Fwpm \* Add0**, **Fwpm \* CreateEnumHandle0**, **Fwpm \* SubscribeChanges0** function Calls, que não podem ser feitas no nível de objeto individual. Para essas funções, há objetos de contêiner para cada tipo de objeto. Para os tipos de objeto padrão (por exemplo, provedores, textos explicativos, filtros), as funções **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0** existentes são sobrecarregadas, de modo que um parâmetro **GUID** nulo identifica o contêiner associado. Para os outros tipos de objeto (por exemplo, eventos de rede e associações de segurança IPsec), há funções explícitas para gerenciar as informações de segurança do contêiner.

O BFE dá suporte à herança automática de ACEs (entradas de controle de acesso) da DACL (lista de controle de acesso discricionário). O BFE não dá suporte a ACEs da lista de controle de acesso (SACL) do sistema. Os objetos herdam ACEs de seu contêiner. Os contêineres herdam ACEs do mecanismo de filtro. Os caminhos de propagação são mostrados no diagrama a seguir.

![Diagrama que mostra os caminhos de propagação da ACE, começando com ' Engine '.](images/access-control.jpg)

Para os tipos de objeto padrão, o BFE impõe todos os direitos de acesso genérico e padrão. Além disso, a WFP define os direitos de acesso específicos a seguir.



| Direito de acesso de WFP                                                                                                                        | Descrição                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**<br/>                                       | Necessário para adicionar um objeto a um contêiner.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Add \_ link**<br/>                       | Necessário para criar uma associação a um objeto. Por exemplo, para adicionar um filtro que faz referência a um texto explicativo, o chamador deve ter o acesso de adicionar \_ link ao texto explicativo.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ begin \_ Read \_ TXN**<br/>    | Necessário para iniciar uma transação de leitura explícita.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ begin \_ Write \_ TXN**<br/> | Necessário para iniciar uma transação de gravação explícita.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ classificar**<br/>                        | Necessário para classificar em uma camada de modo de usuário.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ enum**<br/>                                    | Necessário para enumerar os objetos em um contêiner. No entanto, o enumerador retorna somente os objetos aos quais o chamador tem \_ acesso de leitura FWPM ACTRL \_ .<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**<br/>                                    | Necessário para abrir uma sessão com o BFE.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ leitura**<br/>                                    | Necessário para ler as propriedades de um objeto.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ Read \_ stats**<br/>                 | Necessário para ler estatísticas.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ assinatura**<br/>                     | Necessário para assinar notificações. Os assinantes só receberão notificações para objetos aos quais eles têm acesso de leitura do FWPM \_ ACTRL \_ .<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**<br/>                                 | Necessário para definir as opções do mecanismo.<br/>                                                                                                                               |



 

O BFE ignora todas as verificações de acesso para chamadores de modo kernel.

Para impedir que os administradores bloqueiem o BFE, os membros do grupo de administradores internos sempre recebem **FWPM \_ ACTRL \_ abrir** para o objeto Engine. Portanto, um administrador pode obter acesso por meio das etapas a seguir.

-   habilite o privilégio **ES \_ obter \_ \_ nome de propriedade** .
-   Chame [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). A chamada é realizada com sucesso porque o chamador é membro de administradores internos.
-   Apropriar-se do objeto do mecanismo. isso é executado com sucesso porque o chamador tem o privilégio **ES \_ obter \_ \_ nome de propriedade** .
-   Atualize a DACL. Isso é executado com sucesso porque o proprietário sempre tem acesso de **gravação de \_ DAC**

Como o BFE dá suporte a sua própria auditoria personalizada, ele não gera auditorias de acesso a objetos genéricos. Portanto, a SACL é ignorada.

## <a name="wfp-required-access-rights"></a>Direitos de acesso exigidos pelo WFP

A tabela a seguir mostra os direitos de acesso exigidos pelas funções WFP para acessar vários objetos de plataforma de filtragem. As **\* *funções FwpmFilter _ são listadas como um exemplo para acessar os objetos padrão. Todas as outras funções que acessam objetos padrão seguem o modelo de acesso _* FwpmFilter \*** functions.



Função

Objeto marcado

Acesso necessário

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Mecanismo

**FWPM \_ ACTRL \_ Open**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Mecanismo

**FWPM \_ ACTRL \_ leitura**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Mecanismo

**FWPM \_ ACTRL \_ Write**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Mecanismo

**FWPM \_ ACTRL \_ enum**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Mecanismo

**FWPM \_ ACTRL \_ begin \_ Read \_ TXN**  &  **FWPM \_ ACTRL \_ begin \_ Write \_ TXN**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Provedor de contêiner<br/> Camada<br/> Sub-Layer<br/> Balão<br/> Contexto do provedor<br/>

**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ Adicionar \_ link**<br/> **FWPM \_ ACTRL \_ Add \_ link**<br/> **FWPM \_ ACTRL \_ Add \_ link**<br/> **FWPM \_ ACTRL \_ Add \_ link**<br/> **FWPM \_ ACTRL \_ Add \_ link**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Filtrar

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Filtrar

**FWPM \_ ACTRL \_ leitura**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Filtro de contêiner<br/>

**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ leitura**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Contêiner

**FWPM \_ ACTRL \_ assinatura**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Contêiner

**FWPM \_ ACTRL \_ leitura**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

BANCO de segurança SA IPsec

**FWPM \_ ACTRL \_ Read \_ stats**

[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

BANCO de segurança SA IPsec

**FWPM \_ ACTRL \_ Add**

[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

BANCO de segurança SA IPsec

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

BANCO de segurança SA IPsec

**FWPM \_ ACTRL \_ leitura**

[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

BANCO de segurança SA IPsec

**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

BD SA DE IKE

**FWPM \_ ACTRL \_ Read \_ stats**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

BD SA DE IKE

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

BD SA DE IKE

**FWPM \_ ACTRL \_ leitura**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

BD SA DE IKE

**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Contêiner

**FWPM \_ ACTRL \_ enum**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

Nenhuma verificação de acesso adicional além daquela para os filtros individuais e contextos de provedor



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Direitos de acesso padrão**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[modelo de controle de acesso Windows](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Windows Identificadores de direitos de acesso à plataforma de filtragem**](access-right-identifiers.md)
</dt> </dl>

 

