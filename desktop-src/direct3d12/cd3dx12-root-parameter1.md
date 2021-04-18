---
title: Estrutura de CD3DX12_ROOT_PARAMETER1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura D3D12 raiz \_ parâmetro1.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Estrutura de CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793389"
---
# <a name="cd3dx12_root_parameter1-structure"></a>\_ \_ Estrutura PARÂMETRO1 raiz CD3DX12

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ raiz \_ parâmetro1 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ parâmetro1 raiz CD3DX12 \_ .

</dd> <dt>

**CD3DX12id \_ raiz explícita \_ (const D3D12 \_ raiz \_ parâmetro1 &o)**
</dt> <dd>

Cria uma nova instância de um \_ parâmetro1 raiz CD3DX12 \_ , inicializada com o conteúdo de outra estrutura [**\_ \_ parâmetro1 raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

</dd> <dt>

**estático embutido InitAsDescriptorTable (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* pDescriptorRanges, D3D12 \_ sombreador Visibility \_ visibilidade = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

NumDescriptorRanges UINT

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**estático embutido InitAsConstants (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

Num32BitValues UINT

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**estático embutido InitAsConstantBufferView (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ sinalizadores de \_ descritor de raiz \_ sinalizadores = D3D12 \_ descritor de raiz \_ \_ sinalizador \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ todos)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**estático embutido InitAsShaderResourceView (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ sinalizadores de \_ descritor de raiz \_ sinalizadores = D3D12 \_ descritor de raiz \_ \_ sinalizador \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ todos)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**estático embutido InitAsUnorderedAccessView (D3D12 a \_ raiz \_ parâmetro1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ sinalizadores de \_ descritor de raiz \_ sinalizadores = D3D12 \_ descritor de raiz \_ \_ sinalizador \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ todos)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ RootParam do &\_ PARÂMETRO1 raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsDescriptorTable embutido (UINT numDescriptorRanges, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* pDescriptorRanges, D3D12 \_ Shader \_ visibilidade Visibility = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

NumDescriptorRanges UINT

const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsConstants embutido (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader Visibility \_ VISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

Num32BitValues UINT

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsConstantBufferView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor de raiz \_ sinalizadores = D3D12 do \_ \_ descritor \_ de raiz \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ tudo)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsShaderResourceView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor de raiz \_ sinalizadores = D3D12 do \_ \_ descritor \_ de raiz \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ tudo)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> <dt>

**InitAsUnorderedAccessView embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor de raiz \_ sinalizadores = D3D12 do \_ \_ descritor \_ de raiz \_ nenhum, D3D12 de \_ visibilidade de sombreador \_ = D3D12 a visibilidade do \_ sombreador \_ \_ tudo)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

UINT registerSpace = 0

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum

[**D3D12 \_ Visibilidade de \_ visibilidade do sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = visibilidade D3D12 do \_ sombreador \_ \_

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





