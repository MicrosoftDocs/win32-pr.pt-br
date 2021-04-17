---
title: Estrutura de CD3DX12_ROOT_DESCRIPTOR_TABLE1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura table1 do descritor raiz D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Estrutura de CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761596"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a><span data-ttu-id="83985-104">\_ \_ Estrutura table1 do descritor raiz CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="83985-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1 structure</span></span>

<span data-ttu-id="83985-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ \_ table1 do descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="83985-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="83985-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83985-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="83985-107">Membros</span><span class="sxs-lookup"><span data-stu-id="83985-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="83985-108">**CD3DX12 \_ \_ do descritor raiz \_ Table1 ()**</span><span class="sxs-lookup"><span data-stu-id="83985-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1()**</span></span>
</dt> <dd>

<span data-ttu-id="83985-109">Cria uma nova instância, não inicializada, de um \_ \_ descritor raiz CD3DX12 \_ table1.</span><span class="sxs-lookup"><span data-stu-id="83985-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1.</span></span>

</dd> <dt>

<span data-ttu-id="83985-110">**\_ \_ descritor de raiz CD3DX12 explícito \_ Table1 (const D3D12 \_ raiz \_ Descriptor \_ Table1 &o)**</span><span class="sxs-lookup"><span data-stu-id="83985-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(const D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="83985-111">Cria uma nova instância de um \_ \_ descritor raiz CD3DX12 \_ Table1, inicializada com o conteúdo de outra estrutura [**\_ \_ \_ table1 do descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .</span><span class="sxs-lookup"><span data-stu-id="83985-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="83985-112">**CD3DX12 \_ \_ Descriptor raiz \_ Table1 (UINT NUMDESCRIPTORRANGES, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="83985-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="83985-113">Cria uma nova instância de um \_ \_ descritor raiz CD3DX12 \_ Table1, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="83985-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE1, initializing the following parameters:</span></span>

<span data-ttu-id="83985-114">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="83985-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="83985-115">const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="83985-115">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="83985-116">**Init embutido (UINT numDescriptorRanges, D3D12 const \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="83985-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="83985-117">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="83985-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="83985-118">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="83985-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="83985-119">const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="83985-119">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="83985-120">**Inicialização embutida estática (D3D12 o \_ \_ descritor raiz \_ Table1 &RootDescriptorTable, uint NUMDESCRIPTORRANGES, const D3D12 \_ DESCRIPTOR \_ RANGE1 \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="83985-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="83985-121">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="83985-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="83985-122">[**D3D12 \_ \_Descritor raiz \_ Table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="83985-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable</span></span>

<span data-ttu-id="83985-123">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="83985-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="83985-124">const [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="83985-124">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="83985-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83985-125">Requirements</span></span>



| <span data-ttu-id="83985-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="83985-126">Requirement</span></span> | <span data-ttu-id="83985-127">Valor</span><span class="sxs-lookup"><span data-stu-id="83985-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="83985-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83985-128">Header</span></span><br/> | <dl> <span data-ttu-id="83985-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="83985-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83985-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="83985-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83985-131">**D3D12 \_ do \_ descritor raiz \_ Table1**</span><span class="sxs-lookup"><span data-stu-id="83985-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[<span data-ttu-id="83985-132">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="83985-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





