---
title: Estrutura de CD3DX12_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura desc de assinatura raiz D3D12 \_ .
ms.assetid: A3B820C1-51E8-4E35-A67F-2C4BE82A6B7F
keywords:
- Estrutura de CD3DX12_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f89f9cd0f5ad9be08af1fa9c2556ebfbd4fcff1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798040"
---
# <a name="cd3dx12_root_signature_desc-structure"></a>\_ \_ Estrutura desc de assinatura raiz CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_ROOT_SIGNATURE_DESC  : public D3D12_ROOT_SIGNATURE_DESC{
       CD3DX12_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       CD3DX12_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init(D3D12_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ \_ de assinatura raiz \_ DESC ()**
</dt> <dd>

Cria uma instância nova e não inicializada de uma \_ assinatura raiz CD3DX12 \_ \_ desc.

</dd> <dt>

**\_assinatura raiz CD3DX12 \_ explícita \_ DESC (const D3D12 \_ raiz \_ assinatura \_ desc &o)**
</dt> <dd>

Cria uma nova instância de uma \_ assinatura raiz \_ CD3DX12 \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**CD3DX12 \_ de \_ assinatura raiz \_ DESC (UINT NUMPARAMETERS, const D3D12 \_ raiz \_ parâmetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ assinatura raiz \_ \_ flags = D3D12 sinalizador de \_ assinatura raiz \_ \_ \_ nenhum)**
</dt> <dd>

Cria uma nova instância de uma \_ assinatura raiz \_ CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

NumParameters UINT

[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

opt UINT numStaticSamplers = 0

opt [**D3D12 \_ \_Amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

opt [**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> <dt>

**CD3DX12 \_ \_ de assinatura raiz \_ DESC ( \_ padrão CD3DX12)**
</dt> <dd>

Cria uma nova instância de uma \_ assinatura raiz \_ CD3DX12 \_ DESC, inicializada com os parâmetros padrão.

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

**Init embutido (UINT numParameters, const D3D12 \_ raiz \_ parâmetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ assinatura raiz \_ \_ sinalizadores = D3D12 sinalizador de \_ assinatura raiz \_ \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

NumParameters UINT

[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

opt UINT numStaticSamplers = 0

opt [**D3D12 \_ \_Amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

opt [**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> <dt>

**Inicialização embutida estática ( \_ D3D12 \_ de assinatura raiz \_ desc &DESC, uint NUMPARAMETERS, const D3D12 \_ raiz \_ parâmetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ \_ assinatura raiz \_ sinalizadores = D3D12 \_ sinalizador de \_ assinatura raiz \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ &\_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) desc de assinatura de raiz

NumParameters UINT

[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

opt UINT numStaticSamplers = 0

opt [**D3D12 \_ \_Amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

opt [**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Desc. de \_ assinatura raiz D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





