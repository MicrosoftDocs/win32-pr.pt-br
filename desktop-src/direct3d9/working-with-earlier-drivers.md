---
description: Esta seção lista os problemas que podem ser encontrados ao trabalhar com o Direct3D 9 em drivers escritos para versões do Direct3D anteriores ao Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Trabalhando com drivers anteriores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370097"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Trabalhando com drivers anteriores (Direct3D 9)

Esta seção lista os problemas que podem ser encontrados ao trabalhar com o Direct3D 9 em drivers escritos para versões do Direct3D anteriores ao Direct3D 9.

-   Ao trabalhar com um dispositivo de HAL T&L, a intensidade de neblina é calculada, mas a operação de valor absoluto não é aplicada a esse valor. Em vez disso, o valor será deixado negativo se for o que é calculado. A melhor maneira de evitar essa situação é configurar as transformações adequadamente. Um método menos preferencial é tornar os valores de sombra-início e de neblina negativos para correspondência.

Para verificar um driver do Direct3D 9, procure um valor diferente de zero para D3DDEVCAPS2 \_ STREAMOFFSET no membro DevCaps2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 



