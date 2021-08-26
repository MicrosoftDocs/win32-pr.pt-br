---
description: Um provedor de rede é uma DLL que permite que o Windows operacional para dar suporte a um protocolo de rede específico.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implementando um provedor de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4776bd97b9528bd04bbda25b88e0ff45a8f911429bb573e62dbbb8581abdfbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015976"
---
# <a name="implementing-a-network-provider"></a>Implementando um provedor de rede

Um provedor de rede é uma DLL que permite que o Windows operacional para dar suporte a um protocolo de rede específico. Ele faz isso implementando a API do Provedor de Rede. Essa API é um conjunto de funções que o MPR [*(Roteador De*](../secgloss/m-gly.md) Vários Provedores) chama para se comunicar com a rede. Em seguida, o provedor de rede converte essas chamadas em chamadas à API específicas de rede para executar a ação especificada pela MPR. Dessa forma, o Windows operacional pode interagir com novos protocolos de rede sem precisar entender suas APIs específicas de rede.

Para criar um provedor de rede, escreva uma DLL que exporte a [**função NPGetCaps.**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)

O suporte de outras funções na API do Provedor de Rede é opcional. Se o provedor de rede não exigir uma função, sua DLL não precisará implementá-la nem fornecer uma implementação de stub. Para obter mais informações, consulte os tópicos de função individuais em [Funções do Provedor de Rede](authentication-functions.md).

A exceção é que, se você dá suporte a uma das seguintes funções de enumeração, também deve dar suporte a outras duas funções: [**NPOpenEnum,**](/windows/desktop/api/Npapi/nf-npapi-npopenenum) [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)e [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

As diretrizes a seguir descrevem como escrever um provedor de rede que interaja bem com a MPR e o Windows operacional. Sempre que possível, seu provedor deve seguir as diretrizes a seguir para velocidade, validação e roteamento.

## <a name="speed"></a>Velocidade

Um provedor de rede deve determinar rapidamente se um recurso de rede é seu próprio. Isso porque a MPR pode ter que passar por vários provedores para encontrar o proprietário de um recurso.

Se o provedor de rede não tiver o recurso, ele deverá retornar imediatamente o código de status WN \_ \_ BAD NETNAME.

Também é importante que provedores que deem suporte a [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) retornem resultados para essa função rapidamente porque ela é chamada enquanto WinFile está pintando a árvore de diretório.

## <a name="validation"></a>Validação

A ordem de validação é importante. Um provedor de rede deve primeiro determinar se sua rede é iniciada e, em seguida, determinar se a rede e o provedor de rede são suportados pela operação. Se, após essas verificações, o provedor de rede receber quaisquer recursos de rede, ele deverá determinar se ele os possui. Por fim, ele deve validar outros parâmetros.

## <a name="routing"></a>Roteamento

Se a MPR tiver que passar por provedores de rede, ela tentará todos os provedores até que um aceite a chamada. Em outras palavras, a MPR sempre continua tentando encontrar um provedor de rede.

No entanto, ele observa o primeiro erro significativo relatado por um provedor. Erros como ERROR \_ BAD \_ NETPATH, ERROR \_ BAD NET \_ \_ NAME, ERROR INVALID PARAMETER, ERROR INVALID \_ LEVEL \_ \_ \_ são considerados insignificantes porque simplesmente significam que o provedor não gerencia o recurso. No entanto, se o provedor falhar com o erro ERROR INVALID PASSWORD ou algum outro erro significativo, a MPR registra esse erro e continua a fazer o ciclo pelos \_ \_ provedores de rede. Em geral, ao rotear, se nenhum provedor aceitar a chamada, a MPR relata o primeiro erro significativo encontrado durante o ciclo pelos provedores de rede.

Seu provedor de rede deve levar esse comportamento da MPR em consideração ao decidir qual mensagem de erro retornar.

## <a name="implementation-note"></a>Observação de implementação

Ao implementar DLLs do Provedor de Rede, o provedor não deve chamar outras funções de rede do Windows, [APIs](../shell/samples-usingthumbnailproviders.md)do Shell ou outras consultas baseadas em caminho UNC que podem causar a reentrada no [subsistema](../wnet/windows-networking-functions.md)MPR. Se você fizer essas chamadas de uma DLL do Provedor de Rede, o aplicativo ou outros componentes do sistema operacional poderão ter contenção, baixo desempenho ou deadlocks dentro do subsistema MPR.

 

 
