---
title: Estrutura de CD3DX12_PACKED_MIP_INFO (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de informações MIP empacotada D3D12 \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Estrutura de CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32a4b0516560ac553b3ce6acb6972def5d0e3f84a2eb84026a0635f779a2c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752156"
---
# <a name="cd3dx12_packed_mip_info-structure"></a>\_Estrutura de \_ informações MIP EMPACOTAda CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ \_ informações MIP empacotada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ \_ informações de MIP compactadas \_ ()**
</dt> <dd>

Cria uma nova instância não inicializada de uma \_ informação de MIP empacotada CD3DX12 \_ \_ .

</dd> <dt>

**\_informações explícitas \_ de MIP compactadas do CD3DX12 \_ (const D3D12 \_ informações de MIP empacotadas \_ \_ &o)**
</dt> <dd>

Cria uma nova instância de uma \_ informação de MIP empacotada CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ \_ informações MIP empacotada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .

</dd> <dt>

**CD3DX12 \_ informações de MIP compactadas \_ \_ (UINT8 NumStandardMips, UINT8 NumPackedMips, UINT NumTilesForPackedMips, uint startTileIndexInOverallResource)**
</dt> <dd>

Cria uma nova instância de uma CD3DX12 \_ de \_ informações MIP compactadas \_ , inicializando os seguintes parâmetros:

UINT8 numStandardMips

UINT8 numPackedMips

NumTilesForPackedMips UINT

StartTileIndexInOverallResource UINT

</dd> <dt>

**\_const do operador D3D12 \_ pacotes \_ de informações de MIP compactados& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Informações de \_ MIP compactadas pelo D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





