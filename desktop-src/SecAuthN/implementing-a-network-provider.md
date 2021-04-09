---
description: Um provedor de rede é uma DLL que permite que o sistema operacional Windows dê suporte a um protocolo de rede específico.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implementando um provedor de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97819b033c57feb25cf882f97051785123e2e382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089950"
---
# <a name="implementing-a-network-provider"></a>Implementando um provedor de rede

Um provedor de rede é uma DLL que permite que o sistema operacional Windows dê suporte a um protocolo de rede específico. Ele faz isso implementando a API do provedor de rede. Essa API é um conjunto de funções que o [*roteador do provedor múltiplo*](../secgloss/m-gly.md) (MPR) chama para se comunicar com a rede. O provedor de rede converte essas chamadas em chamadas à API específicas da rede para executar a ação especificada pelo MPR. Dessa forma, o sistema operacional Windows pode interagir com novos protocolos de rede sem precisar entender suas APIs específicas de rede.

Para criar um provedor de rede, grave uma DLL que exporta a função [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) .

O suporte das outras funções na API do provedor de rede é opcional. Se o seu provedor de rede não exigir uma função, sua DLL não precisará implementá-la nem fornecer uma implementação de stub. Para obter mais informações, consulte os tópicos de função individuais em [funções de provedor de rede](authentication-functions.md).

A exceção é que, se você oferecer suporte a uma das seguintes funções de enumeração, deverá oferecer suporte às outras duas funções também: [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)e [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

As diretrizes a seguir descrevem como escrever um provedor de rede que interage bem com o MPR e o sistema operacional Windows. Sempre que possível, seu provedor deve aderir às diretrizes a seguir para velocidade, validação e roteamento.

## <a name="speed"></a>Velocidade

Um provedor de rede deve determinar rapidamente se um recurso de rede é seu. Isso ocorre porque o MPR pode ter que percorrer muitos provedores para localizar o proprietário de um recurso.

Se o provedor de rede não possuir o recurso, ele deverá retornar imediatamente o \_ código de \_ status de NetName do WN inválido.

Também é importante que os provedores que dão suporte ao [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) retornem os resultados para essa função rapidamente, pois ele é chamado enquanto Winfile está pintando a árvore de diretórios.

## <a name="validation"></a>Validação

A ordem de validação é importante. Um provedor de rede deve primeiro determinar se sua rede foi iniciada e, em seguida, determinar se a rede e o provedor de rede dão suporte à operação. Se, após essas verificações, o provedor de rede receber qualquer recurso de rede, ele deverá determinar se ele é proprietário deles. Por fim, ele deve validar outros parâmetros.

## <a name="routing"></a>Roteamento

Se o MPR tiver que percorrer os provedores de rede, ele tentará todos os provedores até que um aceite a chamada. Em outras palavras, o MPR sempre continua a tentar localizar um provedor de rede.

No entanto, ele anota o primeiro erro significativo relatado por um provedor. Erros, como um erro de \_ \_ netpath inválido, erro de \_ \_ nome de rede incorreto \_ , \_ \_ parâmetro de erro inválido, \_ nível inválido de erro \_ são considerados insignificantes porque simplesmente significam que o provedor não gerencia o recurso. No entanto, se o provedor falhar com o erro de erro de \_ senha inválida \_ ou algum outro erro significativo, o MPR registrará esse erro e continuará a percorrer os provedores de rede. Em geral, ao rotear, se nenhum provedor aceitar a chamada, o MPR relatará o primeiro erro significativo que encontrará ao percorrer os provedores de rede.

Seu provedor de rede deve assumir esse comportamento do MPR em conta ao decidir qual mensagem de erro deve ser retornada.

## <a name="implementation-note"></a>Observação de implementação

Ao implementar DLLs do provedor de rede, o provedor não deve chamar outras [funções de rede do Windows](../wnet/windows-networking-functions.md), [APIs de shell](../shell/samples-usingthumbnailproviders.md)ou outras consultas baseadas em caminho UNC que poderiam causar a reentrada no subsistema MPR. Se você fizer essas chamadas de uma DLL de provedor de rede, o aplicativo ou outros componentes do sistema operacional poderão enfrentar contenção, desempenho insatisfatório ou deadlocks dentro do subsistema de MPR.

 

 
