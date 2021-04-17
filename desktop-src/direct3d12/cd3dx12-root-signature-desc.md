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
# <a name="cd3dx12_root_signature_desc-structure"></a><span data-ttu-id="02c6c-104">\_ \_ Estrutura desc de assinatura raiz CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="02c6c-104">CD3DX12\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="02c6c-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="02c6c-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c6c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02c6c-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="02c6c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="02c6c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="02c6c-108">**CD3DX12 \_ \_ de assinatura raiz \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="02c6c-108">**CD3DX12\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="02c6c-109">Cria uma instância nova e não inicializada de uma \_ assinatura raiz CD3DX12 \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="02c6c-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="02c6c-110">**\_assinatura raiz CD3DX12 \_ explícita \_ DESC (const D3D12 \_ raiz \_ assinatura \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="02c6c-110">**explicit CD3DX12\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="02c6c-111">Cria uma nova instância de uma \_ assinatura raiz \_ CD3DX12 \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="02c6c-111">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with the contents of another [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="02c6c-112">**CD3DX12 \_ de \_ assinatura raiz \_ DESC (UINT NUMPARAMETERS, const D3D12 \_ raiz \_ parâmetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ assinatura raiz \_ \_ flags = D3D12 sinalizador de \_ assinatura raiz \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="02c6c-112">**CD3DX12\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="02c6c-113">Cria uma nova instância de uma \_ assinatura raiz \_ CD3DX12 \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="02c6c-113">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="02c6c-114">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="02c6c-114">UINT numParameters</span></span>

<span data-ttu-id="02c6c-115">[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="02c6c-115">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="02c6c-116">opt UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="02c6c-116">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="02c6c-117">opt [**D3D12 \_ \_Amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="02c6c-117">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="02c6c-118">opt [**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="02c6c-118">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="02c6c-119">**CD3DX12 \_ \_ de assinatura raiz \_ DESC ( \_ padrão CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="02c6c-119">**CD3DX12\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="02c6c-120">Cria uma nova instância de uma \_ assinatura raiz \_ CD3DX12 \_ DESC, inicializada com os parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="02c6c-120">Creates a new instance of a CD3DX12\_ROOT\_SIGNATURE\_DESC, initialized with default parameters.</span></span>

``` syntax
CD3DX12_ROOT_SIGNATURE_DESC(0,NULL,0,NULL,D3D12_ROOT_SIGNATURE_FLAG_NONE)
```

</dd> <dt>

<span data-ttu-id="02c6c-121">**Init embutido (UINT numParameters, const D3D12 \_ raiz \_ parâmetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ assinatura raiz \_ \_ sinalizadores = D3D12 sinalizador de \_ assinatura raiz \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="02c6c-121">**inline Init(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="02c6c-122">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="02c6c-122">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="02c6c-123">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="02c6c-123">UINT numParameters</span></span>

<span data-ttu-id="02c6c-124">[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="02c6c-124">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="02c6c-125">opt UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="02c6c-125">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="02c6c-126">opt [**D3D12 \_ \_Amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="02c6c-126">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="02c6c-127">opt [**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="02c6c-127">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="02c6c-128">**Inicialização embutida estática ( \_ D3D12 \_ de assinatura raiz \_ desc &DESC, uint NUMPARAMETERS, const D3D12 \_ raiz \_ parâmetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ \_ assinatura raiz \_ sinalizadores = D3D12 \_ sinalizador de \_ assinatura raiz \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="02c6c-128">**static inline Init(D3D12\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="02c6c-129">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="02c6c-129">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="02c6c-130">[**D3D12 \_ &\_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) desc de assinatura de raiz</span><span class="sxs-lookup"><span data-stu-id="02c6c-130">[**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) &desc</span></span>

<span data-ttu-id="02c6c-131">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="02c6c-131">UINT numParameters</span></span>

<span data-ttu-id="02c6c-132">[**D3D12 \_ \_Parâmetro raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="02c6c-132">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="02c6c-133">opt UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="02c6c-133">(opt) UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="02c6c-134">opt [**D3D12 \_ \_Amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="02c6c-134">(opt) [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="02c6c-135">opt [**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="02c6c-135">(opt) [**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02c6c-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02c6c-136">Requirements</span></span>



| <span data-ttu-id="02c6c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c6c-137">Requirement</span></span> | <span data-ttu-id="02c6c-138">Valor</span><span class="sxs-lookup"><span data-stu-id="02c6c-138">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="02c6c-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02c6c-139">Header</span></span><br/> | <dl> <span data-ttu-id="02c6c-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="02c6c-140"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c6c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="02c6c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c6c-142">**Desc. de \_ assinatura raiz D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="02c6c-142">**D3D12\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="02c6c-143">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="02c6c-143">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





