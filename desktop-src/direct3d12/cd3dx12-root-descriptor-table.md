---
title: Estrutura de CD3DX12_ROOT_DESCRIPTOR_TABLE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de tabela de descritor raiz D3D12 \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Estrutura de CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771323"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a><span data-ttu-id="b3b5b-104">\_Estrutura da \_ tabela do descritor raiz CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="b3b5b-104">CD3DX12\_ROOT\_DESCRIPTOR\_TABLE structure</span></span>

<span data-ttu-id="b3b5b-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ \_ tabela de descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="b3b5b-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3b5b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3b5b-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a><span data-ttu-id="b3b5b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b3b5b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3b5b-108">**\_ \_ Tabela de descritor raiz CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="b3b5b-108">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE()**</span></span>
</dt> <dd>

<span data-ttu-id="b3b5b-109">Cria uma nova instância, não inicializada, de uma \_ tabela de \_ descritor raiz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="b3b5b-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE.</span></span>

</dd> <dt>

<span data-ttu-id="b3b5b-110">**\_ \_ tabela de descritor de raiz CD3DX12 explícita \_ ( \_ tabela de descritores raiz const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="b3b5b-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(const D3D12\_ROOT\_DESCRIPTOR\_TABLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="b3b5b-111">Cria uma nova instância de uma \_ tabela de \_ descritor raiz CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ \_ tabela de descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .</span><span class="sxs-lookup"><span data-stu-id="b3b5b-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3b5b-112">**\_ \_ Tabela do descritor raiz CD3DX12 \_ (UINT NUMDESCRIPTORRANGES, const D3D12 do \_ descritor \_ \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="b3b5b-112">**CD3DX12\_ROOT\_DESCRIPTOR\_TABLE(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="b3b5b-113">Cria uma nova instância de uma \_ tabela de \_ descritor raiz CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b3b5b-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR\_TABLE, initializing the following parameters:</span></span>

<span data-ttu-id="b3b5b-114">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="b3b5b-114">UINT numDescriptorRanges</span></span>

<span data-ttu-id="b3b5b-115">[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b3b5b-115">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="b3b5b-116">**Init embutido (UINT numDescriptorRanges, D3D12 de \_ descritor const \_ \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="b3b5b-116">**inline Init(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="b3b5b-117">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b3b5b-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3b5b-118">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="b3b5b-118">UINT numDescriptorRanges</span></span>

<span data-ttu-id="b3b5b-119">[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b3b5b-119">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> <dt>

<span data-ttu-id="b3b5b-120">**Inicialização embutida estática ( \_ \_ tabela do descritor raiz D3D12 \_ &RootDescriptorTable, uint NUMDESCRIPTORRANGES, const D3D12 do \_ descritor do \_ intervalo \* \_ pDescriptorRanges)**</span><span class="sxs-lookup"><span data-stu-id="b3b5b-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR\_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* \_pDescriptorRanges)**</span></span>
</dt> <dd>

<span data-ttu-id="b3b5b-121">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b3b5b-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b3b5b-122">[**D3D12 \_ \_ \_ Tabela do descritor de raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span><span class="sxs-lookup"><span data-stu-id="b3b5b-122">[**D3D12\_ROOT\_DESCRIPTOR\_TABLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable</span></span>

<span data-ttu-id="b3b5b-123">NumDescriptorRanges UINT</span><span class="sxs-lookup"><span data-stu-id="b3b5b-123">UINT numDescriptorRanges</span></span>

<span data-ttu-id="b3b5b-124">[**D3D12 \_ \_Intervalo de descritores**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b3b5b-124">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* \_pDescriptorRanges</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3b5b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3b5b-125">Requirements</span></span>



| <span data-ttu-id="b3b5b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3b5b-126">Requirement</span></span> | <span data-ttu-id="b3b5b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b3b5b-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b3b5b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3b5b-128">Header</span></span><br/> | <dl> <span data-ttu-id="b3b5b-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3b5b-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3b5b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3b5b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3b5b-131">**\_Tabela de \_ descritor raiz D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="b3b5b-131">**D3D12\_ROOT\_DESCRIPTOR\_TABLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[<span data-ttu-id="b3b5b-132">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="b3b5b-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





