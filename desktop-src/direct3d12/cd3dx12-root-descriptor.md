---
title: Estrutura de CD3DX12_ROOT_DESCRIPTOR (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de descritor raiz D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Estrutura de CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771322"
---
# <a name="cd3dx12_root_descriptor-structure"></a><span data-ttu-id="db89c-104">\_Estrutura do \_ descritor raiz CD3DX12</span><span class="sxs-lookup"><span data-stu-id="db89c-104">CD3DX12\_ROOT\_DESCRIPTOR structure</span></span>

<span data-ttu-id="db89c-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="db89c-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="db89c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db89c-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="db89c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="db89c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="db89c-108">**\_ \_ Descritor raiz CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="db89c-108">**CD3DX12\_ROOT\_DESCRIPTOR()**</span></span>
</dt> <dd>

<span data-ttu-id="db89c-109">Cria uma nova instância, não inicializada, de um \_ descritor de raiz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="db89c-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR.</span></span>

</dd> <dt>

<span data-ttu-id="db89c-110">**\_ \_ descritor de raiz CD3DX12 explícito ( \_ descritor de raiz const D3D12 \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="db89c-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR(const D3D12\_ROOT\_DESCRIPTOR &o)**</span></span>
</dt> <dd>

<span data-ttu-id="db89c-111">Cria uma nova instância de um \_ \_ descritor raiz CD3DX12, inicializada com o conteúdo de outra estrutura de [**\_ \_ descritor raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="db89c-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) structure.</span></span>

</dd> <dt>

<span data-ttu-id="db89c-112">**\_ \_ Descritor raiz CD3DX12 (UINT SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="db89c-112">**CD3DX12\_ROOT\_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="db89c-113">Cria uma nova instância de um \_ \_ descritor raiz CD3DX12, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="db89c-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR, initializing the following parameters:</span></span>

<span data-ttu-id="db89c-114">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="db89c-114">UINT shaderRegister</span></span>

<span data-ttu-id="db89c-115">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="db89c-115">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="db89c-116">**Init embutido (UINT shaderRegister, UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="db89c-116">**inline Init(UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="db89c-117">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="db89c-117">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="db89c-118">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="db89c-118">UINT shaderRegister</span></span>

<span data-ttu-id="db89c-119">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="db89c-119">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="db89c-120">**Inicialização embutida estática ( \_ \_ descritor raiz D3D12 &tabela, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="db89c-120">**static inline Init(D3D12\_ROOT\_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="db89c-121">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="db89c-121">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="db89c-122">[**D3D12 \_ \_Descritor raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &tabela</span><span class="sxs-lookup"><span data-stu-id="db89c-122">[**D3D12\_ROOT\_DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) &table</span></span>

<span data-ttu-id="db89c-123">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="db89c-123">UINT shaderRegister</span></span>

<span data-ttu-id="db89c-124">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="db89c-124">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db89c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db89c-125">Requirements</span></span>



| <span data-ttu-id="db89c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="db89c-126">Requirement</span></span> | <span data-ttu-id="db89c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="db89c-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db89c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db89c-128">Header</span></span><br/> | <dl> <span data-ttu-id="db89c-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="db89c-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db89c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="db89c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db89c-131">**\_ \_ Descritor raiz D3D12**</span><span class="sxs-lookup"><span data-stu-id="db89c-131">**D3D12\_ROOT\_DESCRIPTOR**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[<span data-ttu-id="db89c-132">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="db89c-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





