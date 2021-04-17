---
title: Estrutura de CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura desc de assinatura raiz D3D12 com controle de versão \_ \_ .
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- Estrutura de CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812244"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>\_ \_ \_ Estrutura desc de assinatura raiz CD3DX12 com controle de versão \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ desc de \_ assinatura \_ raiz D3D12 com controle de versão**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ \_ \_ de assinatura de raiz com versão \_ DESC ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ assinatura raiz de versão CD3DX12 \_ \_ \_ desc.

</dd> <dt>

**Explicit CD3DX12 com \_ versão \_ da \_ assinatura raiz \_ DESC (const D3D12 com \_ versão \_ raiz \_ assinatura \_ desc &o)**
</dt> <dd>

Cria uma nova instância de uma assinatura raiz do CD3DX12 com \_ versão \_ \_ \_ DESC, inicializada com o conteúdo de uma estrutura [**\_ \_ \_ \_ desc de assinatura raiz com versão do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

</dd> <dt>

**CD3DX12 explícita \_ \_ \_ de assinatura raiz \_ DESC (const D3D12 \_ assinatura raiz \_ \_ desc &o)**
</dt> <dd>

Cria uma nova instância de uma assinatura raiz do CD3DX12 com \_ versão \_ \_ \_ DESC, inicializada com o conteúdo de uma estrutura [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .

</dd> <dt>

**CD3DX12 explícita \_ \_ \_ de assinatura raiz \_ DESC (const D3D12 \_ assinatura raiz \_ \_ DESC1 &o)**
</dt> <dd>

Cria uma nova instância de uma assinatura raiz de CD3DX12 com \_ controle de versão \_ \_ \_ DESC, inicializada com o conteúdo de uma estrutura de [**\_ \_ \_ DESC1 de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .

</dd> <dt>

**CD3DX12 com \_ versão \_ da \_ assinatura raiz \_ DESC (UINT numParameters, const D3D12 \_ raiz \_ parâmetro \* \_ PPARAMETERS, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de assinatura de \_ raiz \_ \_ flags = D3D12 sinalizador de \_ assinatura raiz \_ \_ \_ nenhum)**
</dt> <dd>

Cria uma nova instância de uma assinatura raiz do CD3DX12 com \_ versão \_ \_ \_ DESC, inicializando os seguintes parâmetros:

NumParameters UINT

[**parâmetro de \_ raiz \_ const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> <dt>

**\_ \_ Assinatura de raiz com versão CD3DX12 \_ \_ DESC (UINT numParameters, const D3D12 \_ root \_ parâmetro1 \* \_ PPARAMETERS, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ assinatura de raiz \_ \_ flags = D3D12 sinalizador de \_ assinatura raiz \_ \_ \_ nenhum)**
</dt> <dd>

Cria uma nova instância de uma assinatura raiz do CD3DX12 com \_ versão \_ \_ \_ DESC, inicializando os seguintes parâmetros:

NumParameters UINT

const [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> <dt>

**CD3DX12 \_ \_ \_ de assinatura raiz \_ de versão DESC ( \_ padrão CD3DX12)**
</dt> <dd>

Cria uma nova instância de uma \_ \_ assinatura raiz do CD3DX12 \_ com versão \_ DESC, inicializada com os parâmetros padrão:

UINT numParameters = 0

const [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = NULL

UINT numStaticSamplers = 0

const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> <dt>

**linha Init \_ 1 \_ 0 (UINT numParameters, const D3D12 \_ raiz \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ estática \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ assinatura de raiz \_ \_ flags = D3D12 \_ sinalizador de \_ assinatura raiz \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

NumParameters UINT

[**parâmetro de \_ raiz \_ const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> <dt>

**estático embutido Init \_ 1 \_ 0 (D3D12 com \_ versão de \_ assinatura raiz \_ \_ desc &DESC, uint numParameters, const D3D12 \_ raiz \_ parâmetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ \_ assinatura raiz \_ sinalizadores = D3D12 \_ sinalizador de assinatura raiz \_ \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ Assinatura de \_ raiz com versão \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc

NumParameters UINT

[**parâmetro de \_ raiz \_ const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> <dt>

**linha inicial embutida \_ 1 \_ 1 (UINT numParameters, const D3D12 \_ root \_ parâmetro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 de \_ sinalizadores de \_ assinatura raiz \_ sinalizadores = D3D12 \_ sinalizador de assinatura raiz \_ \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

NumParameters UINT

const [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> <dt>

**estático embutido Init \_ 1 \_ 1 (D3D12 com \_ versão de \_ assinatura raiz \_ \_ desc &DESC, uint numParameters, const D3D12 \_ raiz \_ parâmetro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ \_ assinatura raiz \_ sinalizadores = D3D12 \_ sinalizador de assinatura raiz \_ \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ Assinatura de \_ raiz com versão \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc

NumParameters UINT

const [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL

[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Desc. de \_ \_ assinatura raiz \_ D3D12 com versão**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





