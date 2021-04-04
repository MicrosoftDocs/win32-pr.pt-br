---
description: Hospedando diretamente um DMO
ms.assetid: 10fb99cf-78d9-4519-9aec-23b0daeca9e2
title: Hospedando diretamente um DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3c933cf4eb946abb9ffefd5186159595480887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646189"
---
# <a name="directly-hosting-a-dmo"></a>Hospedando diretamente um DMO

Esta seção descreve como um aplicativo pode atuar como o cliente direto de um DMO. O aplicativo fornece a entrada para o DMO, o DMO cria a saída, e o aplicativo usa a saída para renderização, processamento adicional ou qualquer outra coisa. O aplicativo é responsável por problemas como alocação de memória, tempo e sincronização e Threading. Esses requisitos dependerão da natureza do aplicativo.

As informações nesta seção também se aplicam se você estiver escrevendo um componente que atue como uma camada entre um aplicativo e um DMO (por exemplo, um controle ActiveX que hospeda um DMO). Além disso, você deve ler esta seção se estiver escrevendo um DMO, pois ela descreve a funcionalidade que o seu DMO deve implementar.

Esta seção contém os seguintes tópicos:

-   [Definindo tipos de mídia em um DMO](setting-media-types-on-a-dmo.md)
-   [Processando dados em um DMO](processing-data-in-a-dmo.md)
-   [Processamento in-loco](in-place-processing.md)
-   [Fluxos opcionais](optional-streams.md)
-   [Implementando IMediaBuffer](implementing-imediabuffer.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DMOs](using-dmos.md)
</dt> </dl>

 

 



