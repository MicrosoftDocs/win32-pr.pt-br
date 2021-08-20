---
title: RWByteAddressBuffer
description: Um buffer de leitura/gravação que indexa em bytes.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- RWByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 931d2592c02b59a38068aa0fe9205d6be7cd1b9a504782f4407144101d09d4ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117905766"
---
# <a name="rwbyteaddressbuffer"></a>RWByteAddressBuffer

Um buffer de leitura/gravação que indexa em bytes.



| Método                                                                                          | Descrição                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [**GetDimensions**](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | Obtém as dimensões do recurso.       |
| [**InterlockedAdd**](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | Adiciona, atomicamente.                   |
| [**InterlockedAnd**](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | ANDs, atomicamente.                   |
| [**InterlockedCompareExchange**](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | Compara e troca, atomicamente. |
| [**InterlockedCompareStore**](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | Compara e armazena, atomicamente.    |
| [**InterlockedExchange**](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | Troca, atomicamente.              |
| [**InterlockedMax**](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | Localiza o máximo, atomicamente.          |
| [**InterlockedMin**](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | Localize o mínimo, atomicamente.           |
| [**Interbloqueador**](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | ORs, atomicamente.                    |
| [**InterlockedXor**](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | XOR, atomicamente.                   |
| [**Carregar**](rwbyteaddressbuffer-load.md)                                                        | Obtém um valor.                     |
| [**Load2**](rwbyteaddressbuffer-load2.md)                                                      | Obtém dois valores.                    |
| [**Load3**](rwbyteaddressbuffer-load3.md)                                                      | Obtém três valores.                  |
| [**Load4**](rwbyteaddressbuffer-load4.md)                                                      | Obtém quatro valores.                   |
| [**Store**](sm5-object-rwbyteaddressbuffer-store.md)                                           | Define um valor.                     |
| [**Store2**](sm5-object-rwbyteaddressbuffer-store2.md)                                         | Define dois valores.                    |
| [**Store3**](sm5-object-rwbyteaddressbuffer-store3.md)                                         | Define três valores.                  |
| [**Store4**](sm5-object-rwbyteaddressbuffer-store4.md)                                         | Define quatro valores.                   |



 

Os objetos RWByteAddressBuffer podem ser prefixados com a classe de armazenamento **globallycoherent**. Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações. Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.

O formato UAV associado a esse recurso precisa ser criado com o formato DXGI \_ \_ R32 \_ formato sem tipo.

O UAV associado a esse recurso deve ter sido criado com o [**\_ sinalizador de UAV de buffer D3D11 \_ \_ \_ bruto**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

Você pode usar o tipo de objeto **RWByteAddressBuffer** ao trabalhar com buffers brutos. Para obter mais informações sobre a exibição bruta de buffers, consulte [exibições brutas de buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Com suporte |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| O [Shader Model 5](d3d11-graphics-reference-sm5.md) e os modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponível por meio da API do Direct3D 11 usando o nível de recurso 10,0 ou 10,1 ([**\_ \_ nível**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)de recurso do D3D \_ 10 \_ X) em dispositivos que dão suporte a sombreadores de computação. Para obter mais informações sobre o suporte de sombreador de computação em hardware de nível inferior, consulte [sombreadores de computação em hardware de nível inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)<br/> | sim       |



 

Este objeto tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

