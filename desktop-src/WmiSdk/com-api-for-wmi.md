---
description: Você pode usar a API do COM (WMI Component Object Model) para gravar aplicativos cliente de gerenciamento ou criar um novo provedor de WMI.
ms.assetid: 5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1
ms.tgt_platform: multiple
title: API COM para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb585badeeeaae947906bbfc783baf355863e05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764545"
---
# <a name="com-api-for-wmi"></a>API COM para WMI

Você pode usar a API do COM (WMI Component Object Model) para gravar aplicativos cliente de gerenciamento ou criar um novo [*provedor*](gloss-p.md)de WMI. A referência da API COM fornece informações para administradores de sistema avançados, bem como os desenvolvedores que estão gravando aplicativos cliente e provedor.

Para obter mais informações sobre como escrever aplicativos de gerenciamento corporativo do WMI, consulte [criando um aplicativo WMI usando C++](creating-a-wmi-application-using-c-.md). Para obter mais informações sobre como escrever um provedor WMI, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).

> [!Note]  
> O WMI só dá suporte ao desenvolvimento C++ usando Microsoft Visual C++ versão 6,0 e sistemas de desenvolvimento posteriores. No entanto, você também pode usar outros compiladores, como os do Borland e do Watcom.

 

Cada um dos diferentes objetos WMI herdam de uma interface, por fim, herdada da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . COM dita como os implementadores de objetos, ou interfaces, lidam com tarefas como gerenciamento de memória, gerenciamento de parâmetros e multithread. Ao estar em conformidade com o COM, a API COM do WMI garante que ele dê suporte à funcionalidade fornecida pelas interfaces de cada objeto WMI.

O WMI é acessado por meio das interfaces COM específicas do WMI a seguir.



| Interface                                                                    | Descrição                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)                         | Enumerador que funciona com objetos do tipo [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject). É semelhante aos enumeradores COM padrão, como [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).                                                                                                      |
| [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)                                         | Implementado por Mofd.dll, essa interface fornece uma interface COM que é usada pelo compilador MOF e quaisquer outros aplicativos que compilam arquivos MOF.                                                                                                                                                       |
| [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)                           | Usado para simplificar o processo de fazer chamadas assíncronas de um processo de cliente.                                                                                                                                                                                                                           |
| [**IWbemBackupRestore**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbembackuprestore)                             | Faz backup e restaura o conteúdo do repositório do WMI.                                                                                                                                                                                                                                                  |
| [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)                                   | Usado para chamadas [semisynchronous](making-a-semisynchronous-call-with-c--.md) da interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Ao fazer essas chamadas, o método de **IWbemServices** chamado retorna imediatamente, juntamente com um objeto [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) .                    |
| [**IWbemCausalityAnalysis**](iwbemcausalityaccess.md)                       | Rastreia solicitações filho que são geradas a partir de uma solicitação pai.                                                                                                                                                                                                                                            |
| [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)                                 | Contém e manipula as definições de classe e as instâncias de objeto de classe. Os desenvolvedores não precisam implementar essa interface; O WMI fornece sua implementação.                                                                                                                                                 |
| [**IWbemConfigureRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemconfigurerefresher)                   | Usado pelo código do cliente para adicionar ou remover enumeradores, objetos e atualizadores aninhados em um atualizador.                                                                                                                                                                                                         |
| [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)                                         | Opcionalmente, usada para comunicar informações de contexto adicionais aos provedores ao enviar chamadas de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ao gerenciamento do Windows.                                                                                                                                             |
| [**IWbemDecoupledBasicEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledbasiceventprovider) | Registra provedores dissociados com o WMI.                                                                                                                                                                                                                                                                    |
| [**IWbemDecoupledRegistrar**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemdecoupledregistrar)                   | Associa provedores desacoplados ao WMI. Essa interface permite que um provedor de processo hospedado defina o tempo de vida da interoperabilidade da interface e coexista com outros provedores.                                                                                                                        |
| [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider)             | Fornece a interface primária para um provedor de consumidor de eventos. Por meio dessa interface e do método [**FindConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventconsumerprovider-findconsumer) , um provedor de consumidor de eventos pode indicar quais consumidores de eventos devem receber um determinado evento.                                          |
| [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider)                             | Usado para iniciar a comunicação com um provedor de eventos.                                                                                                                                                                                                                                                     |
| [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)           | Opcionalmente, implementada por provedores de eventos que desejam saber quais tipos de filtros de consulta de eventos estão ativos no momento para otimizar o desempenho.                                                                                                                                                                 |
| [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity)             | Opcionalmente, implementada por provedores de eventos que desejam restringir o acesso do consumidor ao seu evento.                                                                                                                                                                                                             |
| [**IWbemEventSink**](iwbemeventsink.md)                                     | Inicia a comunicação com um provedor de eventos usando um conjunto restrito de consultas. Essa interface estende o [**IWbemObjectSink**](iwbemobjectsink.md), fornecendo novos métodos que lidam com segurança e desempenho.                                                                                          |
| [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider)                           | Permite que os provedores forneçam objetos e enumeradores atualizáveis.                                                                                                                                                                                                                                           |
| [**IWbemHiPerfEnum**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemhiperfenum)                                   | Usado em operações de atualização para fornecer acesso rápido a enumerações de objetos de instância.                                                                                                                                                                                                                  |
| [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator)                                         | Obtém o ponteiro de namespace inicial para a interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) para WMI em um computador host específico.                                                                                                                                                                         |
| [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess)                               | Fornece acesso aos métodos e às propriedades de um objeto. Um objeto [**IWbemObjectAccess**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjectaccess) é um contêiner para uma instância atualizada por um [*atualizador.*](gloss-r.md)                                                                                           |
| [**IWbemObjectSink**](iwbemobjectsink.md)                                   | Usado para receber os resultados de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) e de certos tipos de notificações de eventos.                                                                                                                                                                                       |
| [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc)                             | Usado para converter instâncias de [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) de e para formatos de texto diferentes.                                                                                                                                                                                               |
| [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider)                       | Dá suporte à recuperação e atualização de propriedades individuais em uma instância de uma classe WMI.                                                                                                                                                                                                                      |
| [**IWbemProviderIdentity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemprovideridentity)                       | Implementado por um provedor de eventos se o provedor se registrar usando mais de um **nome** (várias instâncias do [**\_ \_ Win32Provider**](--win32provider.md)) com o mesmo valor de [CLSID](../com/clsid.md) . A classe fornece um mecanismo para distinguir qual provedor nomeado deve ser usado. |
| [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)                               | Usado para inicializar provedores.                                                                                                                                                                                                                                                                              |
| [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)                       | Implementado pelo WMI e chamado por provedores para relatar o status de inicialização.                                                                                                                                                                                                                                |
| [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset)                               | Atua como um contêiner para todo o conjunto de qualificadores nomeados para uma única propriedade ou objeto inteiro (uma classe ou instância).                                                                                                                                                                                   |
| [**IWbemQuery**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbemquery)                                             | Fornece um ponto de entrada pelo qual uma consulta [*linguagem WQL*](gloss-w.md) (WQL) pode ser analisada.                                                                                                                                                                        |
| [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)                                     | Fornece um ponto de entrada pelo qual objetos atualizáveis, como enumeradores ou objetos de atualização, podem ser atualizados.                                                                                                                                                                                      |
| [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)                                       | Usado por clientes e provedores para acessar os serviços WMI. A interface é implementada somente pelo WMI e é a interface WMI primária.                                                                                                                                                                           |
| [**IWbemStatusCodeText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemstatuscodetext)                           | Extrai descrições de cadeia de caracteres de texto de códigos de erro ou o nome do subsistema em que o erro ocorreu.                                                                                                                                                                                                    |
| [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink)                     | Implementado por todos os consumidores de eventos lógicos. É uma interface de coletor simples que aceita a entrega de objetos de evento.                                                                                                                                                                                          |



 

> [!Note]  
> Muitas das funções COM do WMI retornam códigos de erro numéricos que são documentados como constantes nomeadas. Essas constantes são definidas em Wbemcli. h na pasta PSDK WMI \\ include. Para obter mais informações, consulte [códigos de retorno do WMI](wmi-return-codes.md).

 

Para obter mais informações sobre os tópicos a seguir sobre a programação COM, consulte [desenvolvimento de componentes]( /previous-versions//ee663263(v=vs.85)):

-   Interfaces e design de objeto.
-   Implementando [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   Gerenciamento de memória
-   Tratamento da contagem de referência.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de WMI](wmi-reference.md)
</dt> </dl>

 

 
