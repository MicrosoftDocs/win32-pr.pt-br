---
description: Os aplicativos TAPI residem em seu próprio espaço de processo.
ms.assetid: 57dedad1-7264-48fc-9ac2-c6c72f7fee27
title: Visão geral do provedor de serviços TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e847ed49879e9ff55662477a762fa7297443d12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559741"
---
# <a name="tapi-service-provider-overview"></a>Visão geral do provedor de serviços TAPI

Os aplicativos TAPI residem em seu próprio espaço de processo. Os aplicativos TAPI carregam o Tapi32.dll ou Tapi3.dll em seu processo, e a TAPI se comunica com o TAPISRV por meio de uma interface RPC privada. Um TSP é executado no contexto de TAPISRV. Um determinado TSP pode residir em um computador diferente do computador do usuário e é acessado usando um TSP remoto. O TAPISRV é implementado como um processo de serviço no SVCHOST. Um MSP reside no espaço de processo do aplicativo e sempre é local.

Um par de TSP/MSP pode ser considerado como tendo um caminho de comunicação privada virtual. As informações podem ser enviadas entre os dois usando buffers opacos que não são interpretados pelo TAPISRV ou pela DLL TAPI.

Alguns provedores de serviços implementam operações específicas ao hardware envolvido. A TAPI 2. x fornece acesso a essas operações por meio da função [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) ou [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) . A TAPI 3. x expõe [interfaces específicas do provedor](./provider-specific-interfaces.md).

O diagrama a seguir ilustra o fluxo de controles e informações, mostrando um TSP autônomo (Unimodem) e um par de TSP/MSP (H. 323).

![TSP autônomo e fluxo de dados e controle de TSP/MSP emparelhados](images/tsp-msp1.png)

O diagrama a seguir ilustra o progresso de uma chamada de entrada que envolve um TSP e um MSP.

![chamada de entrada com um TSP e um MSP](images/tspmspin.png)

## <a name="incoming-call-setup"></a>Configuração de chamada de entrada

-   O TSP envia uma mensagem de [**\_ NewCall de linha**](line-newcall.md) para TAPISRV. O [**estado de chamada**](./linecallstate--constants.md) é \_ oferta de LINECALLSTATE.
-   TAPISRV notifica os clientes sobre a chamada.
-   TAPI3 cria o objeto de chamada TAPI e, em seguida, chama [**ITMSPAddress:: CreateMSPCall**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-createmspcall), que é implementado pelo msp.
-   O MSP cria um objeto de chamada MSP e fluxos padrão com base nos [**tipos de mídia**](./tapimediatype--constants.md) necessários para a chamada. Ele retorna um ponteiro IUnknown para o objeto de chamada MSP.
-   TAPI3 agrega o objeto de chamada MSP ao objeto de chamada TAPI, tornando interfaces como [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) disponíveis para o aplicativo. Em seguida, ele notifica a aplicação da nova chamada.

O aplicativo pode então usar métodos como [**ITStream:: SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal) para concluir preparações para a conclusão da chamada.

## <a name="incoming-call-completion"></a>Conclusão de chamada de entrada

-   O aplicativo chama [**ITBasicCallControl:: answer**](/windows/win32/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).
-   TAPI3 chama [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).
-   TAPISERV chama [**TSPI \_ lineAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer).
-   O TSP inicia o streaming de chamadas. Normalmente, o TSP envia uma mensagem para o MSP correspondente e o MSP inicia os fluxos. Em algumas implementações do TSP/MSP, o TSP inicia os fluxos.

## <a name="tspmsp-communication-during-call-progress"></a>Comunicação do TSP/MSP durante o andamento da chamada

Após a chamada estar em andamento, o TSP e o MSP se comunicam passando buffers opacos por meio de TAPISRV e TAPI3.

-   O TSP envia informações para o MSP enviando a mensagem de [**linha \_ SENDMSPDATA**](line-sendmspdata.md) para TAPISRV.
-   O MSP recebe informações do TSP por meio do método [**ITMSPAddress:: ReceiveTSPData**](/windows/win32/api/tapi3/nf-tapi3-itmspaddress-receivetspdata) . Se os dados estiverem relacionados a um objeto de chamada MSP, um ponteiro de interface para o objeto de chamada MSP será fornecido como um parâmetro desse método.
-   O MSP envia informações para o TSP enviando um evento MSP \_ tsp \_ data para TAPI 3.
-   O TSP recebe informações do MSP por meio da função [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata) .

O processo exato e o conteúdo de comunicação entre provedores de serviço é específico para um determinado conjunto de TSP/MSP.

> [!Note]  
> Para chamadas de saída, o MSP normalmente conhece a chamada antes do TSP. Se o MSP tentar se comunicar com o TSP antes que o TSP seja informado sobre uma chamada, a comunicação falhará. Quando o MSP e o TSP precisam trocar informações relacionadas a uma chamada específica, o TSP deve iniciar a comunicação.

 

 

 
