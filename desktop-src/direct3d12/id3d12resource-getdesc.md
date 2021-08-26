---
title: Método GetDesc ID3D12Resource
description: Obtém a descrição do recurso.
ms.assetid: B8D84D69-6B13-4E86-8EF6-A841354B1E5C
keywords:
- Método GetDesc
- Método GetDesc, interface ID3D12Resource
- Interface ID3D12Resource, método GetDesc
topic_type:
- apiref
api_name:
- ID3D12Resource.GetDesc
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
api_location:
- d3d12.h
ms.openlocfilehash: 179acfa051212a2f98eb94441cbfad9fd7d9bbab47e4616f82a4f4cff3d41035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069626"
---
# <a name="id3d12resourcegetdesc-method"></a>Método ID3D12Resource:: GetDesc

Obtém a descrição do recurso.

## <a name="syntax"></a>Sintaxe


```C++
D3D12_RESOURCE_DESC GetDesc();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3D12 do \_ recurso \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)**

Uma estrutura de descrição de recursos do Direct3D 12.

## <a name="examples"></a>Exemplos

Retorna o tamanho necessário de um buffer a ser usado para carregamento de dados.


```C++
// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource->GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource->GetDevice(__uuidof(*pDevice), reinterpret_cast<void**>(&pDevice));
    pDevice->GetCopyableFootprints(&Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &RequiredSize);
    pDevice->Release();
    
    return RequiredSize;
}
```



Consulte o [código de exemplo na referência de D3D12](notes-on-example-code.md).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)
</dt> </dl>

 

 




