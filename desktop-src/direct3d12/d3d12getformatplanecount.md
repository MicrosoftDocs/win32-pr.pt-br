---
title: Função D3D12GetFormatPlaneCount (D3dx12. h)
description: Obtém o número de planos para o formato DXGI especificado para o adaptador virtual especificado (um ID3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- Função D3D12GetFormatPlaneCount
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0791a3326286d6a6e784bc179890258fd7bf320511b37564f538b2d040ed10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098261"
---
# <a name="d3d12getformatplanecount-function"></a>Função D3D12GetFormatPlaneCount

Obtém o número de planos para o formato DXGI especificado para o adaptador virtual especificado (um **ID3D12Device**).

## <a name="syntax"></a>Sintaxe


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***

O adaptador virtual (um [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)) para o qual obter a contagem de planos.

</dd> <dt>

*Formato* 
</dt> <dd>

Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

O [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) para o qual obter a contagem de planos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UINT8**

A contagem de planos para o formato especificado no adaptador virtual especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Informações de \_ formato de dados de recurso D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

