---
title: Funções de alerta
description: As funções de alerta de gerenciamento de rede notificam programas de serviço de rede e aplicativos de eventos de rede.
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411a9bab5f8b74b5dc6e83d9a3c09cdcaeebf66d34c265ad27639e7aab8d7c00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912456"
---
# <a name="alert-functions"></a>Funções de alerta

\[As funções de alerta não têm suporte a partir do Windows Vista porque os serviços do alerter e do messenger não têm suporte.\]

As funções de alerta de gerenciamento de rede notificam programas de serviço de rede e aplicativos de eventos de rede. Um *evento* é uma instância específica de um processo, ocorrência ou estado de hardware conforme definido por um aplicativo. As funções de alerta permitem que os aplicativos indiquem quando eventos predefinidos ocorrem.

**Windows Server 2003:** Os serviços de alerta e de mensagens são desabilitados por padrão Windows Server 2003. Você deve reabilitar os serviços antes de chamar as funções alerta de gerenciamento de rede ou as funções [de mensagem de gerenciamento de rede](message-functions.md).

As funções de alerta são listadas a seguir.



| Função                                   | Descrição                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Notifica todos os clientes registrados de que ocorreu um evento específico.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Simplifica a notificação de clientes registrados de que ocorreu um evento específico, porque, ao contrário de **NetAlertRaise**, **NetAlertRaiseEx** não requer uma estrutura [**de ALERTA \_ STD.**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) |



 

O serviço de alerta deve estar em execução no computador cliente quando você chama a função **NetAlertRaise** ou a **função NetAlertRaiseEx.** Se o serviço não estiver em execução, as funções falharão com **ERROR \_ FILE NOT \_ \_ FOUND**. O serviço de alerta no cliente chama a [**função NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) para enviar informações aos destinatários.

Aplicativos, serviços de rede e componentes de rede internos usam as funções de alerta de gerenciamento de rede para auar um alerta, notificando vários aplicativos ou usuários quando ocorre um determinado tipo de evento. As funções de categoria de alerta, tipos de dados, estruturas e constantes são definidas no LMCONS. H, LTDA. H e LMALERT. Arquivos de header H. Para acessar essas definições, defina as constantes INCL \_ NETERRORS e INCLERRORLERT e inclua o arquivo \_ de header LM.H.

O LMALERT. O arquivo H predefine as seguintes classes de alerta (tipos de eventos de rede) para enviar alertas:

-   Eventos de rede que exigem assistência administrativa
-   Adição de uma entrada a um arquivo de log de erros
-   Recepção de uma mensagem de difusão por um usuário ou um aplicativo
-   Conclusão de um trabalho de impressão
-   Uso de determinados aplicativos ou recursos por usuários

Você pode definir outras classes de alertas para aplicativos de rede conforme necessário. Por exemplo, se um aplicativo em um servidor grava rotineiramente grandes quantidades de dados em uma unidade de disco, o aplicativo corre o risco de preencher o disco. Nesse caso, talvez você queira adicionar o evento "sem espaço livre em disco" para disparar um alerta que notifica o aplicativo para pausar ou encerrar o processo que está preenchendo o disco. O nome do evento para um alerta pode ser qualquer cadeia de caracteres de texto.

Quando você gera um alerta com uma chamada para a função [**NetAlertRaise,**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) os dados da mensagem devem consistir em uma estrutura de título de ALERTA [**STD, \_**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) seguida por dados de comprimento fixo adicionais específicos do alerta em uma outra informação de [**ADMINISTRADOR, \_ \_**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info) [**ERRLOG OTHER \_ \_ INFO**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info), [**IMPRIMIR OUTRAS \_ \_ INFORMAÇÕES**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)ou ESTRUTURA DE OUTRAS INFORMAÇÕES [**\_ \_ DO**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) USUÁRIO. Dados de comprimento variável adicionais podem seguir a estrutura específica do alerta. (Chamadas para a [**função NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) não exigem uma **estrutura de ALERTA \_ STD.)** O aplicativo de chamada deve alocar a memória para todas as estruturas e dados de comprimento variável e liberar a memória após o retorno da chamada.

As macros a seguir estão disponíveis para uso com buffers de dados de alerta.



| Macro                                          | Descrição                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**ALERTA \_ OUTRAS \_ INFORMAÇÕES**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | Retorna um ponteiro para os dados de comprimento fixo que seguem a estrutura **DE ALERTA STD \_** em uma mensagem de alerta. |
| [**DADOS \_ DE VAR DE \_ ALERTA**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | Retorna um ponteiro para os dados de comprimento variável que seguem os dados específicos do alerta em uma mensagem de alerta.   |



 

Em vez de usar as funções de alerta de gerenciamento de rede, você pode usar o SDK do WMI (Instrumentação de Gerenciamento Windows) para notificação de eventos. Para obter mais informações sobre as plataformas que suportam o modelo de evento WMI, consulte Eventos de infraestrutura e monitoramento [WMI](/windows/desktop/WmiSdk/wmi-infrastructure) [na](/windows/desktop/WmiSdk/monitoring-events) documentação do WMI.

 

 