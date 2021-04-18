---
title: Estrutura de CD3DX12_ROOT_CONSTANTS (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de constantes raiz do D3D12 \_ .
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Estrutura de CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771324"
---
# <a name="cd3dx12_root_constants-structure"></a>\_Estrutura de constantes raiz do CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ constantes raiz do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Constantes raiz CD3DX12 \_ ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma das \_ constantes raiz CD3DX12 \_ .

</dd> <dt>

**\_constantes de raiz CD3DX12 explícitas \_ ( \_ constantes de raiz D3D12 const \_ &o)**
</dt> <dd>

Cria uma nova instância de uma CD3DX12 \_ raiz \_ constantes, inicializada com o conteúdo de outra estrutura de [**\_ \_ constantes raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

</dd> <dt>

**CD3DX12 \_ \_ constantes raiz (UINT NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Cria uma nova instância de uma CD3DX12 \_ raiz \_ constantes, inicializando os seguintes parâmetros:

Num32BitValues UINT

ShaderRegister UINT

opt UINT registerSpace = 0

</dd> <dt>

**Init embutido (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

Num32BitValues UINT

ShaderRegister UINT

opt UINT registerSpace = 0

</dd> <dt>

**Inicialização embutida estática ( \_ D3D12 \_ constantes de raiz &ROOTCONSTANTS, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Constantes raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants

Num32BitValues UINT

ShaderRegister UINT

opt UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ \_ constantes raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





