---
title: Estrutura de CD3DX12_ROOT_CONSTANTS (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de constantes raiz do D3D12 \_ .
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Estrutura de CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771324"
---
# <a name="cd3dx12_root_constants-structure"></a><span data-ttu-id="ac160-104">\_Estrutura de constantes raiz do CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="ac160-104">CD3DX12\_ROOT\_CONSTANTS structure</span></span>

<span data-ttu-id="ac160-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ constantes raiz do D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="ac160-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac160-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac160-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="ac160-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ac160-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ac160-108">**\_Constantes raiz CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="ac160-108">**CD3DX12\_ROOT\_CONSTANTS()**</span></span>
</dt> <dd>

<span data-ttu-id="ac160-109">Cria uma nova instância, não inicializada, de uma das \_ constantes raiz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="ac160-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_CONSTANTS.</span></span>

</dd> <dt>

<span data-ttu-id="ac160-110">**\_constantes de raiz CD3DX12 explícitas \_ ( \_ constantes de raiz D3D12 const \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="ac160-110">**explicit CD3DX12\_ROOT\_CONSTANTS(const D3D12\_ROOT\_CONSTANTS &o)**</span></span>
</dt> <dd>

<span data-ttu-id="ac160-111">Cria uma nova instância de uma CD3DX12 \_ raiz \_ constantes, inicializada com o conteúdo de outra estrutura de [**\_ \_ constantes raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .</span><span class="sxs-lookup"><span data-stu-id="ac160-111">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initialized with the contents of another [**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ac160-112">**CD3DX12 \_ \_ constantes raiz (UINT NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="ac160-112">**CD3DX12\_ROOT\_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="ac160-113">Cria uma nova instância de uma CD3DX12 \_ raiz \_ constantes, inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ac160-113">Creates a new instance of a CD3DX12\_ROOT\_CONSTANTS, initializing the following parameters:</span></span>

<span data-ttu-id="ac160-114">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="ac160-114">UINT num32BitValues</span></span>

<span data-ttu-id="ac160-115">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="ac160-115">UINT shaderRegister</span></span>

<span data-ttu-id="ac160-116">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="ac160-116">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="ac160-117">**Init embutido (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="ac160-117">**inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="ac160-118">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ac160-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="ac160-119">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="ac160-119">UINT num32BitValues</span></span>

<span data-ttu-id="ac160-120">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="ac160-120">UINT shaderRegister</span></span>

<span data-ttu-id="ac160-121">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="ac160-121">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="ac160-122">**Inicialização embutida estática ( \_ D3D12 \_ constantes de raiz &ROOTCONSTANTS, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**</span><span class="sxs-lookup"><span data-stu-id="ac160-122">**static inline Init(D3D12\_ROOT\_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="ac160-123">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ac160-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="ac160-124">[**D3D12 \_ \_Constantes raiz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span><span class="sxs-lookup"><span data-stu-id="ac160-124">[**D3D12\_ROOT\_CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants</span></span>

<span data-ttu-id="ac160-125">Num32BitValues UINT</span><span class="sxs-lookup"><span data-stu-id="ac160-125">UINT num32BitValues</span></span>

<span data-ttu-id="ac160-126">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="ac160-126">UINT shaderRegister</span></span>

<span data-ttu-id="ac160-127">opt UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="ac160-127">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac160-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac160-128">Requirements</span></span>



| <span data-ttu-id="ac160-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac160-129">Requirement</span></span> | <span data-ttu-id="ac160-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ac160-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ac160-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac160-131">Header</span></span><br/> | <dl> <span data-ttu-id="ac160-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac160-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac160-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac160-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac160-134">**D3D12 \_ \_ constantes raiz**</span><span class="sxs-lookup"><span data-stu-id="ac160-134">**D3D12\_ROOT\_CONSTANTS**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[<span data-ttu-id="ac160-135">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="ac160-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





