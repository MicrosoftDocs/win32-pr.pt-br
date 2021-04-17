---
description: Como é mencionado na visão geral do identificador de sessão, um identificador de chamada é o meio pelo qual um aplicativo TAPI 2,2 identifica uma sessão de comunicação específica.
ms.assetid: 5f6a7adf-c074-4bf6-9828-76604eb7609c
title: Identificadores de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacad5b73d9d22caa006b734acaf8b992203d7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789876"
---
# <a name="call-handles"></a>Identificadores de chamada

Como é mencionado na visão geral do [identificador de sessão](./session-identifier-ovr.md) , um identificador de chamada é o meio pelo qual um aplicativo TAPI 2,2 identifica uma sessão de comunicação específica. Quando um aplicativo inicia uma sessão, a TAPI retorna um identificador de chamada para uso em operações ou consultas adicionais. Quando um aplicativo é notificado de uma sessão de entrada, a TAPI também passa em um identificador de chamada.

Depois que uma sessão for encerrada e o estado da sessão estiver ocioso, o identificador de chamada permanecerá válido até que o aplicativo desaloque o identificador ou a linha seja fechada. A linha pode ser fechada pelo aplicativo ou pode receber uma mensagem de [**\_ fechamento de linha**](line-close.md) . Se uma linha for fechada, todos os identificadores de chamada para chamadas na linha se tornarão instantaneamente inválidos.

Depois que uma chamada reverte para o estado *ocioso* , o aplicativo ainda tem permissão para ler a estrutura de informações e o status da chamada. Isso permite que os aplicativos usem operações como [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para recuperar informações de chamada para fins de log.

Quando o aplicativo não tem mais nenhum uso para o identificador de uma chamada ociosa, ele deve chamar [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) para liberar a memória alocada pelo sistema relacionada à chamada. A TAPI aloca memória para cada chamada para cada aplicativo que tem um identificador para a chamada. É provável que os provedores de serviços aloquem memória para manter as informações de chamada também. A desalocação do identificador de chamada de um aplicativo permite que a biblioteca e o provedor de serviços recuperem esses recursos de memória. O identificador de um aplicativo para uma chamada se torna nulo após uma desalocação bem-sucedida.

O aplicativo deve, em si, liberar memória relacionada à chamada alocada para suas próprias finalidades.

 

 
