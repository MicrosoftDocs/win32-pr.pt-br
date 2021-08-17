---
title: Métodos TextureCube::TextureCube Gather
description: Retorna os quatro valores de texel que seriam usados em uma operação de filtragem bi-linear. | Métodos TextureCube::TextureCube Gather
ms.assetid: 4891A62A-9D54-4F7E-92C2-9CDDF1453671
keywords:
- Coletar métodos HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 4dfc4e6ecee3c78b0b0419c6b2525558f7d0122487630695aaace48873da91df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786814"
---
# <a name="texturecubegather-methods"></a>Métodos TextureCube::Gather

Retorna os quatro valores de texel que seriam usados em uma operação de filtragem bi-linear.

Consulte a documentação [sobre gather4](./gather4--sm5---asm-.md) para obter mais informações que descrevem a instrução DXBC subjacente.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                     | Descrição                                                                                                              |
|:-----------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [**Gather(S,float)**](dx-graphics-hlsl-to-gather.md)      | Amostra uma textura e retorna as quatro amostras (somente componente vermelho) que são usadas para interpolação bilinear.<br/> |
| [**Gather(S,float,uint)**](tcube-gather-s-float-uint-.md) | Amostra uma textura e retorna todos os quatro componentes junto com o status sobre a operação.<br/>                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

