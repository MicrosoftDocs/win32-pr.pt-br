---
title: Estrutura de CD3DX12_ROOT_PARAMETER (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de parâmetro raiz D3D12 \_ .
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Estrutura de CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798041"
---
# <a name="cd3dx12_root_parameter-structure"></a>\_Estrutura de \_ parâmetro raiz CD3DX12

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ parâmetro raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Parâmetro raiz CD3DX12 \_ ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ parâmetro raiz CD3DX12 \_ .

</dd> <dt>

**\_parâmetro raiz CD3DX12 explícito \_ (parâmetro const D3D12 \_ raiz \_ &o)**
</dt> <dd>

Cria uma nova instância de um \_ parâmetro raiz CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ parâmetro raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

</dd> <dt>

**estático embutido InitAsDescriptorTable (D3D12 de \_ parâmetro de raiz \_ &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ intervalo \* pDescriptorRanges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsConstants embutido estático ( \_ parâmetro de raiz D3D12 \_ &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

Num32BitValues UINT

ShaderRegister UINT

opt UINT registerSpace = 0

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsConstantBufferView embutido estático ( \_ parâmetro de raiz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

ShaderRegister UINT

opt UINT registerSpace = 0

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsShaderResourceView embutido estático ( \_ parâmetro de raiz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

ShaderRegister UINT

opt UINT registerSpace = 0

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsUnorderedAccessView embutido estático ( \_ parâmetro de raiz D3D12 \_ &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

ShaderRegister UINT

opt UINT registerSpace = 0

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsDescriptorTable embutido (UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ intervalo \* pDescriptorRanges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

NumDescriptorRanges UINT

[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsConstants embutido (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader Visibility \_ VISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

Num32BitValues UINT

ShaderRegister UINT

opt UINT registerSpace = 0

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsConstantBufferView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ sombreador de visibilidade \_ visibilidade = D3D12 de \_ visibilidade do sombreador \_ \_ tudo)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

opt UINT registerSpace = 0

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsShaderResourceView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ sombreador de visibilidade \_ visibilidade = D3D12 de \_ visibilidade do sombreador \_ \_ tudo)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

opt UINT registerSpace = 0

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsUnorderedAccessView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ sombreador de visibilidade \_ visibilidade = D3D12 de \_ visibilidade do sombreador \_ \_ tudo)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

opt UINT registerSpace = 0

opt [**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Parâmetro raiz \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





