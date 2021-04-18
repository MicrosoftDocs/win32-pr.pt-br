---
title: Estrutura de CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de informações de alocação de recursos D3D12 \_ \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Estrutura de CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807980"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a><span data-ttu-id="4ce59-104">\_Estrutura de \_ informações de alocação de recursos CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="4ce59-104">CD3DX12\_RESOURCE\_ALLOCATION\_INFO structure</span></span>

<span data-ttu-id="4ce59-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ informações de \_ alocação \_ de recursos D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="4ce59-105">A helper structure to enable easy initialization of a [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce59-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ce59-106">Syntax</span></span>


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="4ce59-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4ce59-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ce59-108">**\_ \_ \_ Informações de alocação de recursos do CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="4ce59-108">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="4ce59-109">Cria uma nova instância, não inicializada, de uma \_ informação de alocação de recurso CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4ce59-109">Creates a new, uninitialized, instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="4ce59-110">**\_ \_ informações de alocação de recursos CD3DX12 explícitas \_ (const D3D12 \_ informações de alocação de recursos \_ \_& o)**</span><span class="sxs-lookup"><span data-stu-id="4ce59-110">**explicit CD3DX12\_RESOURCE\_ALLOCATION\_INFO(const D3D12\_RESOURCE\_ALLOCATION\_INFO& o)**</span></span>
</dt> <dd>

<span data-ttu-id="4ce59-111">Cria uma nova instância de uma \_ informação de alocação de recursos CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de informações de [**alocação de recursos do D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .</span><span class="sxs-lookup"><span data-stu-id="4ce59-111">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initialized with the contents of another [**D3D12\_RESOURCE\_ALLOCATION\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4ce59-112">**\_ \_ \_ Informações de alocação de recursos CD3DX12 (tamanho de UInt64, alinhamento de UInt64)**</span><span class="sxs-lookup"><span data-stu-id="4ce59-112">**CD3DX12\_RESOURCE\_ALLOCATION\_INFO(UINT64 size, UINT64 alignment)**</span></span>
</dt> <dd>

<span data-ttu-id="4ce59-113">Cria uma nova instância de uma \_ informação de alocação de recursos CD3DX12 \_ \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="4ce59-113">Creates a new instance of a CD3DX12\_RESOURCE\_ALLOCATION\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="4ce59-114">Tamanho de UINT64</span><span class="sxs-lookup"><span data-stu-id="4ce59-114">UINT64 size</span></span>

<span data-ttu-id="4ce59-115">Alinhamento de UINT64</span><span class="sxs-lookup"><span data-stu-id="4ce59-115">UINT64 alignment</span></span>

</dd> <dt>

<span data-ttu-id="4ce59-116">**const D3D12 \_ \_ \_& informações de alocação de recurso**</span><span class="sxs-lookup"><span data-stu-id="4ce59-116">**operator const D3D12\_RESOURCE\_ALLOCATION\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="4ce59-117">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="4ce59-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ce59-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ce59-118">Requirements</span></span>



| <span data-ttu-id="4ce59-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ce59-119">Requirement</span></span> | <span data-ttu-id="4ce59-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4ce59-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce59-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ce59-121">Header</span></span><br/> | <dl> <span data-ttu-id="4ce59-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ce59-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ce59-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ce59-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ce59-124">**\_Informações de \_ alocação de recursos do D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4ce59-124">**D3D12\_RESOURCE\_ALLOCATION\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[<span data-ttu-id="4ce59-125">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="4ce59-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





