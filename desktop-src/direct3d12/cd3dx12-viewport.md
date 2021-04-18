---
title: Estrutura de CD3DX12_VIEWPORT (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura viewport D3D12.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Estrutura de CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791610"
---
# <a name="cd3dx12_viewport-structure"></a><span data-ttu-id="0059c-104">\_Estrutura do visor CD3DX12</span><span class="sxs-lookup"><span data-stu-id="0059c-104">CD3DX12\_VIEWPORT structure</span></span>

<span data-ttu-id="0059c-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0059c-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0059c-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0059c-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0059c-107">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ viewport D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .</span><span class="sxs-lookup"><span data-stu-id="0059c-107">A helper structure to enable easy initialization of a [**D3D12\_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="0059c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0059c-108">Syntax</span></span>


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a><span data-ttu-id="0059c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="0059c-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="0059c-110">**\_Visor CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="0059c-110">**CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="0059c-111">Cria uma instância nova e não inicializada de um visor CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="0059c-111">Creates a new, uninitialized, instance of a CD3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="0059c-112">**visor CD3DX12 explícito \_ (const D3D12 \_ viewport& o)**</span><span class="sxs-lookup"><span data-stu-id="0059c-112">**explicit CD3DX12\_VIEWPORT(const D3D12\_VIEWPORT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="0059c-113">Cria uma nova instância de um \_ visor CD3DX12, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="0059c-113">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="0059c-114">const D3D12 \_ VIEWPORT& o</span><span class="sxs-lookup"><span data-stu-id="0059c-114">const D3D12\_VIEWPORT& o</span></span>

</dd> <dt>

<span data-ttu-id="0059c-115">**visor CD3DX12 explícito \_ (float topLeftX, float topLeftY, largura de float, altura flutuante, float minDepth = D3D12 \_ min \_ Depth, float MaxDepth = D3D12 \_ Max \_ Depth)**</span><span class="sxs-lookup"><span data-stu-id="0059c-115">**explicit CD3DX12\_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="0059c-116">Cria uma nova instância de um \_ visor CD3DX12, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="0059c-116">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="0059c-117">TopLeftX flutuante</span><span class="sxs-lookup"><span data-stu-id="0059c-117">FLOAT topLeftX</span></span>

<span data-ttu-id="0059c-118">TopLeftY flutuante</span><span class="sxs-lookup"><span data-stu-id="0059c-118">FLOAT topLeftY</span></span>

<span data-ttu-id="0059c-119">Largura flutuante</span><span class="sxs-lookup"><span data-stu-id="0059c-119">FLOAT width</span></span>

<span data-ttu-id="0059c-120">Altura do FLOAT</span><span class="sxs-lookup"><span data-stu-id="0059c-120">FLOAT height</span></span>

<span data-ttu-id="0059c-121">FLOAT minDepth = \_ profundidade mínima de D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="0059c-121">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="0059c-122">FLOAT maxDepth = \_ profundidade máxima de D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="0059c-122">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="0059c-123">**visor CD3DX12 explícito \_ (ID3D12Resource \* de origem, uint mipSlice = 0, float topLeftX = 0,0 f, float topLeftY = 0,0 f, float MINDEPTH = D3D12 \_ min \_ Depth, float MaxDepth = D3D12 \_ Max \_ Depth)**</span><span class="sxs-lookup"><span data-stu-id="0059c-123">**explicit CD3DX12\_VIEWPORT(ID3D12Resource\* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="0059c-124">Cria uma nova instância de um \_ visor CD3DX12, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="0059c-124">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="0059c-125">ID3D12Resource de \* origem</span><span class="sxs-lookup"><span data-stu-id="0059c-125">ID3D12Resource\* pResource</span></span>

<span data-ttu-id="0059c-126">UINT mipSlice = 0</span><span class="sxs-lookup"><span data-stu-id="0059c-126">UINT mipSlice = 0</span></span>

<span data-ttu-id="0059c-127">FLOAT topLeftX = 0,0 f</span><span class="sxs-lookup"><span data-stu-id="0059c-127">FLOAT topLeftX = 0.0f</span></span>

<span data-ttu-id="0059c-128">FLOAT topLeftY = 0,0 f</span><span class="sxs-lookup"><span data-stu-id="0059c-128">FLOAT topLeftY = 0.0f</span></span>

<span data-ttu-id="0059c-129">FLOAT minDepth = \_ profundidade mínima de D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="0059c-129">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="0059c-130">FLOAT maxDepth = \_ profundidade máxima de D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="0059c-130">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="0059c-131">**~ CD3DX12 \_ viewport ()**</span><span class="sxs-lookup"><span data-stu-id="0059c-131">**~CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="0059c-132">Destrói uma instância de um visor D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="0059c-132">Destroys an instance of a D3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="0059c-133">**\_const do operador D3D12 VIEWPORT& () constante**</span><span class="sxs-lookup"><span data-stu-id="0059c-133">**operator const D3D12\_VIEWPORT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="0059c-134">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="0059c-134">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0059c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0059c-135">Requirements</span></span>



| <span data-ttu-id="0059c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0059c-136">Requirement</span></span> | <span data-ttu-id="0059c-137">Valor</span><span class="sxs-lookup"><span data-stu-id="0059c-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0059c-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0059c-138">Header</span></span><br/> | <dl> <span data-ttu-id="0059c-139"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="0059c-139"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0059c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0059c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0059c-141">**\_Visor D3D12**</span><span class="sxs-lookup"><span data-stu-id="0059c-141">**D3D12\_VIEWPORT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[<span data-ttu-id="0059c-142">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="0059c-142">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





