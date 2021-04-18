---
title: Estrutura de CD3DX12_STATIC_SAMPLER_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura desc de amostra estática D3D12 \_ .
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- Estrutura de CD3DX12_STATIC_SAMPLER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768255"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a>\_ \_ Estrutura desc de amostra estática CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ \_ desc de amostra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Amostra de CD3DX12 estática \_ DESC ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma amostra de CD3DX12 \_ estática \_ \_ desc.

</dd> <dt>

**\_amostras estáticas CD3DX12 explícita \_ \_ DESC (const D3D12 de \_ \_ amostra estática \_ desc &o)**
</dt> <dd>

Cria uma nova instância de uma \_ amostra CD3DX12 \_ estática \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ \_ desc de amostra estática D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .

</dd> <dt>

**CD3DX12 \_ \_ de amostra estática \_ DESC (UINT shaderRegister, \_ filtro de filtro D3D12 = D3D12 \_ filtro \_ ANISOTROPIC, D3D12 \_ textura de endereço modo endereçou = D3D12 modo de \_ \_ \_ \_ endereço de textura \_ \_ encapsulado, D3D12 \_ modo de endereço de textura \_ \_ addressV = D3D12 \_ \_ \_ modo de endereço de textura com \_ encapsulamento, \_ \_ \_ modo de endereço de textura D3D12 addressW = \_ \_ \_ modo de endereço de textura de D3D12 \_ encapsulado, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func COMPARISONFUNC = D3D12 \_ comparation \_ Func \_ \_ Equals, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaco \_ , float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ visibilidade \_ All, uint registerSpace**
</dt> <dd>

Cria uma nova instância de uma \_ amostra CD3DX12 \_ estática \_ DESC, inicializando os seguintes parâmetros:

ShaderRegister UINT

opt [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) \_ filtro D3D12 \_ ANISOTROPIC

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressexception = modo de endereço de textura de D3D12 \_ \_ \_ \_ Wrap

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12

opt FLOAT mipLODBias = 0

opt UINT maxAnisotropy = 16

opt [**D3D12 \_ COMPARAÇÃO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ Comparison \_ Func \_ menos \_ igual

opt [**D3D12 \_ \_ \_ Cor da borda estática**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 de \_ \_ borda estática \_ cor \_ \_ branco opaco

opt FLOAT minLOD = 0. f

opt FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

opt [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All

opt UINT registerSpace = 0

</dd> <dt>

**Inicialização embutida estática ( \_ D3D12 \_ de amostra de estática \_ desc &SamplerDesc, uint shaderRegister, D3D12 \_ filtro filtro = D3D12 \_ filtro \_ ANISOTROPIC, D3D12 \_ modo de endereço de textura \_ \_ endereçou = D3D12 modo \_ de endereço de textura de \_ \_ encapsulado, D3D12 modo de endereço de textura addressV \_ \_ \_ \_ = D3D12 \_ \_ \_ modo de endereço de textura \_ \_ \_ \_ modo de endereço de textura D3D12 addressW = \_ \_ \_ modo de endereço de textura de D3D12 \_ encapsulado, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func COMPARISONFUNC = D3D12 \_ comparation \_ Func \_ \_ Equals, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaco \_ , float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ visibilidade \_ All, uint registerSpace**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_Amostra \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) de samplerDesc &desc de forma estática

ShaderRegister UINT

opt [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) \_ filtro D3D12 \_ ANISOTROPIC

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressexception = modo de endereço de textura de D3D12 \_ \_ \_ \_ Wrap

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12

opt FLOAT mipLODBias = 0

opt UINT maxAnisotropy = 16

opt [**D3D12 \_ COMPARAÇÃO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ Comparison \_ Func \_ menos \_ igual

opt [**D3D12 \_ \_ \_ Cor da borda estática**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 de \_ \_ borda estática \_ cor \_ \_ branco opaco

opt FLOAT minLOD = 0. f

opt FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

opt [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All

opt UINT registerSpace = 0

</dd> <dt>

**Init embutido (UINT shaderRegister, filtro de \_ filtro D3D12 = D3D12 \_ filtro \_ ANISOTROPIC, D3D12 \_ modo de endereço de textura \_ \_ endereçou = D3D12 modo de endereço \_ de textura \_ de D3D12 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ modo de endereço de textura D3D12 addressW = \_ \_ \_ modo de endereço de textura de D3D12 \_ encapsulado, float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonFunc = D3D12 \_ comparation \_ Func \_ \_ Equals, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static \_ Border \_ Color \_ opaco \_ , float minLOD = 0. f, float maxLOD = D3D12 \_ FLOAT32 \_ Max, D3D12 \_ Shader \_ Visibility shaderVisibility = D3D12 \_ Shader \_ visibilidade \_ All, uint registerSpace**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

ShaderRegister UINT

opt [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) \_ filtro D3D12 \_ ANISOTROPIC

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressexception = modo de endereço de textura de D3D12 \_ \_ \_ \_ Wrap

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12

opt [**D3D12 \_ \_ \_ Modo de endereço de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ \_ encapsulamento do modo de endereço de textura D3D12

opt FLOAT mipLODBias = 0

opt UINT maxAnisotropy = 16

opt [**D3D12 \_ COMPARAÇÃO \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) COMPARISONFUNC = D3D12 \_ Comparison \_ Func \_ menos \_ igual

opt [**D3D12 \_ \_ \_ Cor da borda estática**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 de \_ \_ borda estática \_ cor \_ \_ branco opaco

opt FLOAT minLOD = 0. f

opt FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max

opt [**D3D12 \_ SHADER \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 \_ Shader \_ visibilidade \_ All

opt UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Amostra de D3D12 \_ estática \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





