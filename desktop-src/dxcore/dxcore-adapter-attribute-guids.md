---
title: GUIDs de atributo do adaptador de DXCore
description: 'As seguintes GUIDs de atributo de adaptador são declaradas em `dxcore_interface.h` e são usadas com os métodos [IDXCoreAdapterFactory:: createadapterlist](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter:: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) .'
keywords:
- DXCore, atributo de adaptador, GUIDs
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a532552f144dfc21aa5d6a368aecd915d30b40c8
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/31/2021
ms.locfileid: "106098489"
---
# <a name="dxcore-adapter-attribute-guids"></a>GUIDs de atributo do adaptador de DXCore

As seguintes GUIDs de atributo de adaptador são declaradas em `dxcore_interface.h` e são usadas com os métodos [IDXCoreAdapterFactory:: createadapterlist](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter:: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) . Para qualquer adaptador, um ou mais dos atributos podem ser aplicados.

| GUID | Valor |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Especifica um adaptador que oferece suporte para uso com as APIs de gráficos do [Direct3D 11](/windows/win32/direct3d11) . Nenhuma garantia é feita sobre recursos específicos, nem uma garantia de que o sistema operacional em sua configuração atual dê suporte a essas APIs. | 0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Especifica um adaptador que oferece suporte para uso com as APIs de gráficos do [Direct3D 12](/windows/win32/direct3d12) . Nenhuma garantia é feita sobre recursos específicos, nem uma garantia de que o sistema operacional em sua configuração atual dê suporte a essas APIs. | 0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1B, 0x47, 0xB1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Especifica um adaptador que oferece suporte para uso com as APIs de computação [principal do Direct3D 12](../direct3d12/core-feature-levels.md) . Nenhuma garantia é feita sobre recursos específicos, nem uma garantia de que o sistema operacional em sua configuração atual dê suporte a essas APIs. | 0x248e2800, 0xa793, 0x4724, 0xab, 0xAA, 0x23, 0xA6, 0xde, 0x1B, 0xE0, 0x90 |

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | dxcore_interface. h |

## <a name="see-also"></a>Confira também

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [Referência de DXCore](./dxcore-reference.md)
* [Usar DXCore para enumerar adaptadores](./dxcore-enum-adapters.md)
* [Gráficos do Direct3D 12](../direct3d12/direct3d-12-graphics.md)
