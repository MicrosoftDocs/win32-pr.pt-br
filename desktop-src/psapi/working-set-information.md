---
title: Informações do conjunto de trabalho
description: O conjunto de trabalho de um processo é a quantidade de memória mapeada fisicamente para seu contexto de processo. O PSAPI permite que você tire instantâneos do conjunto de trabalho ou monitore o conjunto de trabalho.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3942796ec1150dee411d6074b13f9ee2be4a22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084803"
---
# <a name="working-set-information"></a>Informações do conjunto de trabalho

O conjunto de trabalho de um processo é a quantidade de memória mapeada fisicamente para seu contexto de processo. O PSAPI permite que você tire instantâneos do conjunto de trabalho ou monitore o conjunto de trabalho.

A função [**QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) ou [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) preenche um buffer com um instantâneo das informações de cada página no conjunto de trabalho atual do processo especificado. A função relata apenas as páginas fisicamente presentes no momento exato em que são chamadas.

Você pode usar o monitoramento de conjunto de trabalho para descobrir a quantidade de RAM adicional que uma operação específica leva (por exemplo, salvar um arquivo). Para começar a monitorar o conjunto de trabalho, chame a função [**InitializeProcessForWsWatch**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) . Nem todos os processos permitem que você leia suas informações de conjunto de trabalho, portanto, certifique-se de que a função retorna um valor diferente de zero antes de continuar. Em seguida, chame a função [**GetWsChanges**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) . Essa função relata apenas as páginas que foram carregadas na memória desde que você começou a monitorar o conjunto de trabalho. A função retorna dados em uma matriz de estruturas de [**\_ informações de \_ inspeção \_ do WS psapi**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) , uma estrutura para cada nova página adicionada ao conjunto de trabalho do processo. A estrutura informa quais páginas estão na memória e o que fez com que o sistema a Pagesse.

A função [**EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) usa um identificador de processo. Ele remove o máximo de páginas possível do conjunto de trabalho do processo. Essa operação é útil principalmente para teste e ajuste. Observe que a função [**SetProcessWorkingSetSize**](/windows/desktop/api/winbase/nf-winbase-setprocessworkingsetsize) faz a mesma coisa se você passá-la-1 para os tamanhos mínimo e máximo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjunto de trabalho](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 