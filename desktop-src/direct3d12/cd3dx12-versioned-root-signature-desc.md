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
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a><span data-ttu-id="8b244-104">\_ \_ \_ Estrutura desc de assinatura raiz CD3DX12 com controle de versão \_</span><span class="sxs-lookup"><span data-stu-id="8b244-104">CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC structure</span></span>

<span data-ttu-id="8b244-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ desc de \_ assinatura \_ raiz D3D12 com controle de versão**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="8b244-105">A helper structure to enable easy initialization of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b244-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b244-106">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="8b244-107">Membros</span><span class="sxs-lookup"><span data-stu-id="8b244-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8b244-108">**CD3DX12 \_ \_ \_ de assinatura de raiz com versão \_ DESC ()**</span><span class="sxs-lookup"><span data-stu-id="8b244-108">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-109">Cria uma nova instância, não inicializada, de uma \_ assinatura raiz de versão CD3DX12 \_ \_ \_ desc.</span><span class="sxs-lookup"><span data-stu-id="8b244-109">Creates a new, uninitialized, instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="8b244-110">**Explicit CD3DX12 com \_ versão \_ da \_ assinatura raiz \_ DESC (const D3D12 com \_ versão \_ raiz \_ assinatura \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="8b244-110">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-111">Cria uma nova instância de uma assinatura raiz do CD3DX12 com \_ versão \_ \_ \_ DESC, inicializada com o conteúdo de uma estrutura [**\_ \_ \_ \_ desc de assinatura raiz com versão do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="8b244-111">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b244-112">**CD3DX12 explícita \_ \_ \_ de assinatura raiz \_ DESC (const D3D12 \_ assinatura raiz \_ \_ desc &o)**</span><span class="sxs-lookup"><span data-stu-id="8b244-112">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-113">Cria uma nova instância de uma assinatura raiz do CD3DX12 com \_ versão \_ \_ \_ DESC, inicializada com o conteúdo de uma estrutura [**\_ \_ \_ desc de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) .</span><span class="sxs-lookup"><span data-stu-id="8b244-113">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b244-114">**CD3DX12 explícita \_ \_ \_ de assinatura raiz \_ DESC (const D3D12 \_ assinatura raiz \_ \_ DESC1 &o)**</span><span class="sxs-lookup"><span data-stu-id="8b244-114">**explicit CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(const D3D12\_ROOT\_SIGNATURE\_DESC1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-115">Cria uma nova instância de uma assinatura raiz de CD3DX12 com \_ controle de versão \_ \_ \_ DESC, inicializada com o conteúdo de uma estrutura de [**\_ \_ \_ DESC1 de assinatura raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) .</span><span class="sxs-lookup"><span data-stu-id="8b244-115">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the contents of a [**D3D12\_ROOT\_SIGNATURE\_DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b244-116">**CD3DX12 com \_ versão \_ da \_ assinatura raiz \_ DESC (UINT numParameters, const D3D12 \_ raiz \_ parâmetro \* \_ PPARAMETERS, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de assinatura de \_ raiz \_ \_ flags = D3D12 sinalizador de \_ assinatura raiz \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="8b244-116">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-117">Cria uma nova instância de uma assinatura raiz do CD3DX12 com \_ versão \_ \_ \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8b244-117">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="8b244-118">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="8b244-118">UINT numParameters</span></span>

<span data-ttu-id="8b244-119">[**parâmetro de \_ raiz \_ const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="8b244-119">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="8b244-120">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="8b244-120">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="8b244-121">const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="8b244-121">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="8b244-122">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8b244-122">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="8b244-123">**\_ \_ Assinatura de raiz com versão CD3DX12 \_ \_ DESC (UINT numParameters, const D3D12 \_ root \_ parâmetro1 \* \_ PPARAMETERS, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ assinatura de raiz \_ \_ flags = D3D12 sinalizador de \_ assinatura raiz \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="8b244-123">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-124">Cria uma nova instância de uma assinatura raiz do CD3DX12 com \_ versão \_ \_ \_ DESC, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8b244-124">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="8b244-125">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="8b244-125">UINT numParameters</span></span>

<span data-ttu-id="8b244-126">const [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="8b244-126">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="8b244-127">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="8b244-127">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="8b244-128">const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="8b244-128">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="8b244-129">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8b244-129">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="8b244-130">**CD3DX12 \_ \_ \_ de assinatura raiz \_ de versão DESC ( \_ padrão CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="8b244-130">**CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-131">Cria uma nova instância de uma \_ \_ assinatura raiz do CD3DX12 \_ com versão \_ DESC, inicializada com os parâmetros padrão:</span><span class="sxs-lookup"><span data-stu-id="8b244-131">Creates a new instance of a CD3DX12\_VERSIONED\_ROOT\_SIGNATURE\_DESC, initialized with the default parameters:</span></span>

<span data-ttu-id="8b244-132">UINT numParameters = 0</span><span class="sxs-lookup"><span data-stu-id="8b244-132">UINT numParameters = 0</span></span>

<span data-ttu-id="8b244-133">const [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = NULL</span><span class="sxs-lookup"><span data-stu-id="8b244-133">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters = NULL</span></span>

<span data-ttu-id="8b244-134">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="8b244-134">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="8b244-135">const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="8b244-135">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="8b244-136">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8b244-136">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="8b244-137">**linha Init \_ 1 \_ 0 (UINT numParameters, const D3D12 \_ raiz \_ Parameter \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ estática \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ assinatura de raiz \_ \_ flags = D3D12 \_ sinalizador de \_ assinatura raiz \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="8b244-137">**inline Init\_1\_0(UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-138">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8b244-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8b244-139">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="8b244-139">UINT numParameters</span></span>

<span data-ttu-id="8b244-140">[**parâmetro de \_ raiz \_ const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="8b244-140">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="8b244-141">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="8b244-141">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="8b244-142">const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="8b244-142">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="8b244-143">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8b244-143">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="8b244-144">**estático embutido Init \_ 1 \_ 0 (D3D12 com \_ versão de \_ assinatura raiz \_ \_ desc &DESC, uint numParameters, const D3D12 \_ raiz \_ parâmetro \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ \_ assinatura raiz \_ sinalizadores = D3D12 \_ sinalizador de assinatura raiz \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="8b244-144">**static inline Init\_1\_0(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-145">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8b244-145">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8b244-146">[**D3D12 \_ Assinatura de \_ raiz com versão \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span><span class="sxs-lookup"><span data-stu-id="8b244-146">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="8b244-147">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="8b244-147">UINT numParameters</span></span>

<span data-ttu-id="8b244-148">[**parâmetro de \_ raiz \_ const D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="8b244-148">const [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)\* \_pParameters</span></span>

<span data-ttu-id="8b244-149">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="8b244-149">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="8b244-150">const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="8b244-150">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="8b244-151">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8b244-151">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="8b244-152">**linha inicial embutida \_ 1 \_ 1 (UINT numParameters, const D3D12 \_ root \_ parâmetro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 de \_ sinalizadores de \_ assinatura raiz \_ sinalizadores = D3D12 \_ sinalizador de assinatura raiz \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="8b244-152">**inline Init\_1\_1(UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-153">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8b244-153">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8b244-154">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="8b244-154">UINT numParameters</span></span>

<span data-ttu-id="8b244-155">const [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="8b244-155">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="8b244-156">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="8b244-156">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="8b244-157">const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="8b244-157">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="8b244-158">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8b244-158">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="8b244-159">**estático embutido Init \_ 1 \_ 1 (D3D12 com \_ versão de \_ assinatura raiz \_ \_ desc &DESC, uint numParameters, const D3D12 \_ raiz \_ parâmetro1 \* \_ pParameters, uint numStaticSamplers = 0, const D3D12 \_ static \_ Sample \_ desc \* \_ pStaticSamplers = NULL, D3D12 sinalizadores de \_ \_ assinatura raiz \_ sinalizadores = D3D12 \_ sinalizador de assinatura raiz \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="8b244-159">**static inline Init\_1\_1(D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC &desc, UINT numParameters, const D3D12\_ROOT\_PARAMETER1\* \_pParameters, UINT numStaticSamplers = 0, const D3D12\_STATIC\_SAMPLER\_DESC\* \_pStaticSamplers = NULL, D3D12\_ROOT\_SIGNATURE\_FLAGS flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="8b244-160">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8b244-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="8b244-161">[**D3D12 \_ Assinatura de \_ raiz com versão \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span><span class="sxs-lookup"><span data-stu-id="8b244-161">[**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc</span></span>

<span data-ttu-id="8b244-162">NumParameters UINT</span><span class="sxs-lookup"><span data-stu-id="8b244-162">UINT numParameters</span></span>

<span data-ttu-id="8b244-163">const [**D3D12 \_ raiz \_ parâmetro1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters</span><span class="sxs-lookup"><span data-stu-id="8b244-163">const [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)\* \_pParameters</span></span>

<span data-ttu-id="8b244-164">UINT numStaticSamplers = 0</span><span class="sxs-lookup"><span data-stu-id="8b244-164">UINT numStaticSamplers = 0</span></span>

<span data-ttu-id="8b244-165">const [**D3D12 \_ de \_ amostra estática \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = NULL</span><span class="sxs-lookup"><span data-stu-id="8b244-165">const [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)\* \_pStaticSamplers = NULL</span></span>

<span data-ttu-id="8b244-166">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de assinatura raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) = \_ sinalizador de assinatura raiz D3D12 \_ \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="8b244-166">[**D3D12\_ROOT\_SIGNATURE\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) flags = D3D12\_ROOT\_SIGNATURE\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8b244-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b244-167">Requirements</span></span>



| <span data-ttu-id="8b244-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b244-168">Requirement</span></span> | <span data-ttu-id="8b244-169">Valor</span><span class="sxs-lookup"><span data-stu-id="8b244-169">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8b244-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b244-170">Header</span></span><br/> | <dl> <span data-ttu-id="8b244-171"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b244-171"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b244-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b244-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b244-173">**\_Desc. de \_ \_ assinatura raiz \_ D3D12 com versão**</span><span class="sxs-lookup"><span data-stu-id="8b244-173">**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[<span data-ttu-id="8b244-174">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="8b244-174">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





