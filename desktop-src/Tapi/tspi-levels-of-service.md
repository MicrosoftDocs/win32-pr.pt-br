---
description: A TAPI divide os serviços de comunicação em básico, complementar e estendido. Consulte os níveis de serviço TAPI para obter informações adicionais.
ms.assetid: e2e6b113-b6b0-43a1-ac95-6e8e188a6120
title: TSPI níveis de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c72f09f7a076364918815ba5fdb79591f6f5b12382ac2aa529e0859eec53f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012126"
---
# <a name="tspi-levels-of-service"></a>TSPI níveis de serviço

A TAPI divide os serviços de comunicação em básico, complementar e estendido. Consulte [os níveis de serviço TAPI](./tapi-levels-of-service.md) para obter informações adicionais.

Um TSP é necessário para implementar todas as funções de telefonia básicas. As [funções de telefonia básicas do TSPI](tspi-basic-telephony-functions.md) contêm um resumo dessas funções.

A telefonia suplementar inclui recursos encontrados em PBXs modernos, como retenção, transferência, conferência, estacionamento e assim por diante. Um provedor de serviços deve fornecer um serviço de telefonia suplementar somente se ele puder implementar o significado exato conforme definido pela TAPI. Caso contrário, o recurso deve ser fornecido como um serviço de telefonia estendido. Todos os recursos complementares são opcionais. Um provedor de serviços especifica quais serviços ele dá suporte por meio de respostas a funções como [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) ou [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). Um único serviço suplementar pode consistir em várias chamadas de função e mensagens. Telefone serviços de dispositivo fazem parte da telefonia suplementar.

Serviços de telefonia estendidos permitem que um provedor implemente funções específicas do dispositivo. O provedor de serviços deve identificar exclusivamente as extensões usando um *identificador de extensão*. Os aplicativos recuperam e usam esse identificador exclusivo para determinar as extensões às quais o provedor de serviços dá suporte.

As extensões podem ser aplicadas a vários fabricantes. Funções e mensagens especiais, como [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) e [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) , são fornecidas na TAPI. Eles são usados para permitir a extensão do conjunto de funções (em contraste com enumerações, sinalizadores de bits e membros da estrutura de dados) com suporte do provedor de serviços. Os parâmetros para cada função também são definidos pelo provedor de serviços.

Um identificador é atribuído a um conjunto de extensões (antes da distribuição), não a cada instância individual de uma implementação dessas extensões. O utilitário EXTIDGEN no TSPI gera identificadores de extensão exclusivos para provedores de serviço. Ele usa um endereço de adaptador Ethernet, um número aleatório e a hora do dia para gerar um identificador, portanto, é extremamente improvável que o identificador de extensão resultante entre em conflito com qualquer outro provedor de serviços. Como resultado, não há necessidade de que os fornecedores registrem identificadores de extensão.

O utilitário EXTIDGEN não gera identificadores de extensão, a menos que o computador no qual ele é executado também esteja executando NetBIOS ou outro software de rede.

 

 
