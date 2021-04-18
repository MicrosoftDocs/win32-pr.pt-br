---
title: Estrutura de CD3DX12_BOX (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de caixa D3D12.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Estrutura de CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807158"
---
# <a name="cd3dx12_box-structure"></a><span data-ttu-id="19847-104">Estrutura da caixa de CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="19847-104">CD3DX12\_BOX structure</span></span>

<span data-ttu-id="19847-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ caixa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="19847-105">A helper structure to enable easy initialization of a [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="19847-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19847-106">Syntax</span></span>


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a><span data-ttu-id="19847-107">Membros</span><span class="sxs-lookup"><span data-stu-id="19847-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="19847-108">**\_Caixa de CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="19847-108">**CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="19847-109">Cria uma nova instância, não inicializada, de uma \_ caixa CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="19847-109">Creates a new, uninitialized, instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="19847-110">**caixa CD3DX12 explícita \_ (const D3D12 \_ Box& o)**</span><span class="sxs-lookup"><span data-stu-id="19847-110">**explicit CD3DX12\_BOX(const D3D12\_BOX& o)**</span></span>
</dt> <dd>

<span data-ttu-id="19847-111">Cria uma nova instância de uma \_ caixa CD3DX12, inicializada com o conteúdo de outra estrutura de [**\_ caixa de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="19847-111">Creates a new instance of a CD3DX12\_BOX, initialized with the contents of another [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

</dd> <dt>

<span data-ttu-id="19847-112">**caixa CD3DX12 explícita \_ (esquerda longa, longa direita)**</span><span class="sxs-lookup"><span data-stu-id="19847-112">**explicit CD3DX12\_BOX(LONG Left, LONG Right)**</span></span>
</dt> <dd>

<span data-ttu-id="19847-113">Cria uma nova instância de uma \_ caixa CD3DX12, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="19847-113">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="19847-114">LONGA para a esquerda</span><span class="sxs-lookup"><span data-stu-id="19847-114">LONG Left</span></span>

<span data-ttu-id="19847-115">LONGO direito</span><span class="sxs-lookup"><span data-stu-id="19847-115">LONG Right</span></span>

</dd> <dt>

<span data-ttu-id="19847-116">**caixa CD3DX12 explícita \_ (esquerda longa, longa superior, longa direita, longa parte inferior)**</span><span class="sxs-lookup"><span data-stu-id="19847-116">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="19847-117">Cria uma nova instância de uma \_ caixa CD3DX12, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="19847-117">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="19847-118">LONGA para a esquerda</span><span class="sxs-lookup"><span data-stu-id="19847-118">LONG Left</span></span>

<span data-ttu-id="19847-119">Início longo</span><span class="sxs-lookup"><span data-stu-id="19847-119">LONG Top</span></span>

<span data-ttu-id="19847-120">LONGO direito</span><span class="sxs-lookup"><span data-stu-id="19847-120">LONG Right</span></span>

<span data-ttu-id="19847-121">Parte inferior longa</span><span class="sxs-lookup"><span data-stu-id="19847-121">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="19847-122">**caixa CD3DX12 explícita \_ (longa esquerda, longa superior, frente longo, longa direita, longa parte inferior, longa volta)**</span><span class="sxs-lookup"><span data-stu-id="19847-122">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**</span></span>
</dt> <dd>

<span data-ttu-id="19847-123">Cria uma nova instância de uma \_ caixa CD3DX12, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="19847-123">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="19847-124">LONGA para a esquerda</span><span class="sxs-lookup"><span data-stu-id="19847-124">LONG Left</span></span>

<span data-ttu-id="19847-125">Início longo</span><span class="sxs-lookup"><span data-stu-id="19847-125">LONG Top</span></span>

<span data-ttu-id="19847-126">Frente longo</span><span class="sxs-lookup"><span data-stu-id="19847-126">LONG Front</span></span>

<span data-ttu-id="19847-127">LONGO direito</span><span class="sxs-lookup"><span data-stu-id="19847-127">LONG Right</span></span>

<span data-ttu-id="19847-128">Parte inferior longa</span><span class="sxs-lookup"><span data-stu-id="19847-128">LONG Bottom</span></span>

<span data-ttu-id="19847-129">LONGO retorno</span><span class="sxs-lookup"><span data-stu-id="19847-129">LONG Back</span></span>

</dd> <dt>

<span data-ttu-id="19847-130">**~ CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="19847-130">**~CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="19847-131">Destrói uma instância de uma caixa CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="19847-131">Destroys an instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="19847-132">**\_const da& caixa D3D12 de operador const () constante**</span><span class="sxs-lookup"><span data-stu-id="19847-132">**operator const D3D12\_BOX&() const**</span></span>
</dt> <dd>

<span data-ttu-id="19847-133">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="19847-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19847-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19847-134">Requirements</span></span>



| <span data-ttu-id="19847-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="19847-135">Requirement</span></span> | <span data-ttu-id="19847-136">Valor</span><span class="sxs-lookup"><span data-stu-id="19847-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="19847-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19847-137">Header</span></span><br/> | <dl> <span data-ttu-id="19847-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="19847-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19847-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="19847-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19847-140">**Caixa de D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="19847-140">**D3D12\_BOX**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[<span data-ttu-id="19847-141">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="19847-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





