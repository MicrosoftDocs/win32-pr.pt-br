---
title: troca dinâmica de dados
description: esta seção fornece diretrizes para implementar o intercâmbio de dados dinâmicos para aplicativos que não podem usar a biblioteca de gerenciamento de troca dinâmica de dados (DDEML).
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- troca dinâmica de dados (DDE), sobre
- DDE (troca dinâmica de dados), sobre
- troca de dados, troca dinâmica de dados (DDE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db58f1027f0dfaacf28c4b2ec8d4208747929b0d40ca55d7d377831777f78a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678036"
---
# <a name="dynamic-data-exchange"></a>troca dinâmica de dados

esta seção fornece diretrizes para implementar o intercâmbio de dados dinâmicos para aplicativos que não podem usar a biblioteca de gerenciamento de troca dinâmica de dados (DDEML). para obter mais informações sobre o DDEML, consulte [troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md).

### <a name="overviews"></a>Visões gerais



| Nome                                                           | Descrição                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [Sobre troca dinâmica de dados](about-dynamic-data-exchange.md) | Discute a transferência de dados entre aplicativos.<br/>       |
| [Usando troca dinâmica de dados](using-dynamic-data-exchange.md) | Fornece exemplos de código relacionados à troca de dados dinâmicas.<br/> |
| [Referência DDE](dynamic-data-exchange-reference.md)           | A referência da API.<br/>                                      |



 

### <a name="dde-functions"></a>Funções DDE



| Nome                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | especifica a QOS (qualidade de serviço) que um aplicativo de troca dinâmica de dados bruto (DDE) desejar para futuras conversas de DDE que iniciar. A QOS especificada se aplica a qualquer conversa iniciada enquanto essas configurações estiverem em vigor. A qualidade de serviço de uma conversa DDE dura a duração da conversa; as chamadas para a função [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) durante uma conversa não afetam a QoS da conversa. <br/> |
| [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | Libera a memória especificada pelo parâmetro *lParam* de uma mensagem DDE postada. Um aplicativo que recebe uma mensagem DDE postada deve chamar essa função depois de ter usado a função [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) para descompactar o valor de *lParam* . <br/>                                                                                                                                                                                                     |
| [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | Permite que um aplicativo de servidor DDE represente o contexto de segurança de um aplicativo cliente DDE. Isso protege os dados do servidor seguro contra clientes DDE não autorizados. <br/>                                                                                                                                                                                                                                                                                                      |
| [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | Compacta um valor de *lParam* DDE em uma estrutura interna usada para compartilhar dados DDE entre processos.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | Permite que um aplicativo reutilize um parâmetro DDE *lParam* empacotado, em vez de alocar um novo *lParam* embalado. O uso dessa função reduz as realocações para aplicativos que passam mensagens DDE empacotadas. <br/>                                                                                                                                                                                                                                                          |
| [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | Desempacota um valor de *lParam* DDE recebido de uma mensagem DDE postada. <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>Mensagens DDE



| Nome                                         | Descrição                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**início do WM \_ DDE \_**](wm-dde-initiate.md) | Inicia uma conversa com um aplicativo de servidor respondendo aos nomes de aplicativo e tópico especificados. Ao receber essa mensagem, todos os aplicativos de servidor com nomes que correspondem ao aplicativo especificado e que dão suporte ao tópico especificado devem confirmá-lo.<br/> |



 

### <a name="dde-notifications"></a>Notificações DDE



| Nome                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACK de DDE do WM \_**](wm-dde-ack.md)             | Nnotifies um aplicativo DDE do recebimento e processamento das seguintes mensagens: [**WM \_ DDE \_**](wm-dde-poke.md)enviar, [**WM \_ DDE \_ Execute**](wm-dde-execute.md), WM DDE [**\_ \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ Advise**](wm-dde-advise.md), WM DDE [**\_ \_ UNADVISE**](wm-dde-unadvise.md), WM DDE [**\_ \_ INITIATE**](wm-dde-initiate.md)ou o [**WM \_ DDE \_ Request**](wm-dde-request.md) (em alguns casos). <br/> |
| [**\_aviso de DDE do WM \_**](wm-dde-advise.md)       | Um aplicativo cliente DDE posta a mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) em um aplicativo de servidor DDE para solicitar que o servidor forneça uma atualização para um item de dados sempre que o item for alterado. <br/>                                                                                                                                                                                                              |
| [**\_dados DDE do WM \_**](wm-dde-data.md)           | Um aplicativo de servidor DDE posta uma mensagem de [**\_ \_ dados DDE do WM**](wm-dde-data.md) em um aplicativo cliente DDE para passar um item de dados para o cliente ou notificar o cliente sobre a disponibilidade de um item de dados. <br/>                                                                                                                                                                                                           |
| [**\_execução de DDE do WM \_**](wm-dde-execute.md)     | Um aplicativo cliente DDE posta uma mensagem de [**\_ \_ execução do WM DDE**](wm-dde-execute.md) em um aplicativo de servidor DDE para enviar uma cadeia de caracteres ao servidor a ser processada como uma série de comandos. Espera-se que o aplicativo de servidor poste uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) em resposta. <br/>                                                                                                                      |
| [**o WM \_ DDE. \_**](wm-dde-poke.md)           | Um aplicativo cliente DDE posta uma mensagem de envio [**\_ \_ DDE do WM**](wm-dde-poke.md) para um aplicativo de servidor DDE. Um cliente usa essa mensagem para solicitar que o servidor aceite um item de dados não solicitado. Espera-se que o servidor responda com uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) indicando se ele aceitou o item de dados. <br/>                                                                                   |
| [**\_solicitação de DDE do WM \_**](wm-dde-request.md)     | Um aplicativo cliente DDE posta uma mensagem de [**\_ \_ solicitação de DDE do WM**](wm-dde-request.md) em um aplicativo de servidor DDE para solicitar o valor de um item de dados. <br/>                                                                                                                                                                                                                                                              |
| [**fim do WM \_ DDE \_**](wm-dde-terminate.md) | Um aplicativo DDE (cliente ou servidor) posta uma mensagem de [**\_ \_ encerramento de DDE do WM**](wm-dde-terminate.md) para encerrar uma conversa. <br/>                                                                                                                                                                                                                                                                                  |
| [**\_aviso de DDE do WM \_**](wm-dde-unadvise.md)   | Um aplicativo cliente DDE posta uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-unadvise.md) para informar a um aplicativo de servidor DDE que o item especificado ou um formato de área de transferência específico para o item não deve mais ser atualizado. Isso encerra o link de dados quente ou ativo para o item especificado. <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>Estruturas DDE



| Nome                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | Contém sinalizadores de status que um aplicativo DDE passa para seu parceiro como parte da mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) . Os sinalizadores fornecem detalhes sobre a resposta do aplicativo para as mensagens [**\_ \_ dados DDE do WM**](wm-dde-data.md), o [**WM \_ DDE \_**](wm-dde-poke.md)enviar, o WM [**\_ DDE \_ Execute**](wm-dde-execute.md), o [**WM \_ DDE \_ Advise**](wm-dde-advise.md), o [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)e a [**\_ \_ solicitação DDE do WM**](wm-dde-request.md). <br/> |
| [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | Contém sinalizadores que especificam como um aplicativo de servidor DDE deve enviar dados para um aplicativo cliente durante um loop de aviso. Um cliente passa um identificador para uma estrutura [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) para um servidor como parte de uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) . <br/>                                                                                                                                                                                               |
| [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)     | Contém os dados e informações sobre os dados, enviados como parte de uma mensagem [**de \_ \_ dados DDE do WM**](wm-dde-data.md) . <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | Contém os dados e informações sobre os dados, enviados como parte de uma mensagem de envio [**\_ \_ DDE do WM**](wm-dde-poke.md) . <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | Contém um nome de serviço DDE e um nome de tópico. Um aplicativo de servidor DDE pode usar essa estrutura durante uma transação [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) para enumerar os pares de Service-topic aos quais ele dá suporte. <br/>                                                                                                                                                                                                                                                   |



 

 

 





