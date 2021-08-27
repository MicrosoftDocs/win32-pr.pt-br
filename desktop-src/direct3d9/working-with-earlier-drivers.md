---
description: Esta seção lista os problemas que podem ser encontrados ao trabalhar com o Direct3D 9 em drivers escritos para versões do Direct3D anteriores ao Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Trabalhando com drivers anteriores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24284c706d49ce3294e23486f72150ffd74ee376e2be0d7d06dca09877eb7cc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796905"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Trabalhando com drivers anteriores (Direct3D 9)

Esta seção lista os problemas que podem ser encontrados ao trabalhar com o Direct3D 9 em drivers escritos para versões do Direct3D anteriores ao Direct3D 9.

-   Ao trabalhar com um dispositivo T&L HAL, a intensidade da bateria é calculada, mas a operação de valor absoluto não é aplicada a esse valor. Em vez disso, o valor será deixado negativo se for o que é calculado. A melhor maneira de evitar essa situação é configurar as transformaçãos adequadamente. Um método menos preferencial é tornar os valores de ponto de partida e de término negativos para corresponder.

Para verificar se há um driver Direct3D 9, procure um valor diferente de zero para D3DDEVCAPS2 STREAMOFFSET no membro \_ DevCaps2 [**de D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Programação Dicas](programming-tips.md)
</dt> </dl>

 

 



