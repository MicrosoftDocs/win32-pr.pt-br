---
title: Estrutura de CD3DX12_ROOT_DESCRIPTOR1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura DESCRIPTOR1 raiz D3D12.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Estrutura de CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814406"
---
# <a name="cd3dx12_root_descriptor1-structure"></a><span data-ttu-id="da8d6-104">\_Estrutura de \_ DESCRIPTOR1 raiz CD3DX12</span><span class="sxs-lookup"><span data-stu-id="da8d6-104">CD3DX12\_ROOT\_DESCRIPTOR1 structure</span></span>

<span data-ttu-id="da8d6-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ DESCRIPTOR1 raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="da8d6-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="da8d6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da8d6-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a><span data-ttu-id="da8d6-107">Membros</span><span class="sxs-lookup"><span data-stu-id="da8d6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="da8d6-108">**CD3DX12 \_ raiz \_ DESCRIPTOR1 ()**</span><span class="sxs-lookup"><span data-stu-id="da8d6-108">**CD3DX12\_ROOT\_DESCRIPTOR1()**</span></span>
</dt> <dd>

<span data-ttu-id="da8d6-109">Cria uma nova instância, não inicializada, de uma \_ DESCRIPTOR1 raiz CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="da8d6-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_DESCRIPTOR1.</span></span>

</dd> <dt>

<span data-ttu-id="da8d6-110">**CD3DX12 \_ \_ DESCRIPTOR1 (const D3D12 \_ raiz \_ DESCRIPTOR1 &o)**</span><span class="sxs-lookup"><span data-stu-id="da8d6-110">**explicit CD3DX12\_ROOT\_DESCRIPTOR1(const D3D12\_ROOT\_DESCRIPTOR1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="da8d6-111">Cria uma nova instância de uma \_ DESCRIPTOR1 raiz CD3DX12 \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ DESCRIPTOR1 raiz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .</span><span class="sxs-lookup"><span data-stu-id="da8d6-111">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initialized with the contents of another [**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="da8d6-112">**CD3DX12 \_ raiz \_ DESCRIPTOR1 (UINT SHADERREGISTER, uint registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor raiz \_ flags = D3D12 \_ sinalizador do \_ descritor raiz \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="da8d6-112">**CD3DX12\_ROOT\_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="da8d6-113">Cria uma nova instância de uma \_ DESCRIPTOR1 raiz CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="da8d6-113">Creates a new instance of a CD3DX12\_ROOT\_DESCRIPTOR1, initializing the following parameters:</span></span>

<span data-ttu-id="da8d6-114">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="da8d6-114">UINT shaderRegister</span></span>

<span data-ttu-id="da8d6-115">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="da8d6-115">UINT registerSpace = 0</span></span>

<span data-ttu-id="da8d6-116">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="da8d6-116">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="da8d6-117">**Init embutido (UINT shaderRegister, UINT registerSpace = 0, D3D12 sinalizadores do \_ \_ descritor de raiz \_ sinalizadores = D3D12 \_ sinalizador do \_ descritor raiz \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="da8d6-117">**inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="da8d6-118">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="da8d6-118">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="da8d6-119">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="da8d6-119">UINT shaderRegister</span></span>

<span data-ttu-id="da8d6-120">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="da8d6-120">UINT registerSpace = 0</span></span>

<span data-ttu-id="da8d6-121">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="da8d6-121">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> <dt>

<span data-ttu-id="da8d6-122">**Inicialização embutida estática (D3D12 \_ raiz \_ DESCRIPTOR1 &tabela, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ sinalizadores de descritor de raiz \_ \_ sinalizadores = \_ sinalizador de descritor raiz D3D12 \_ \_ \_ nenhum)**</span><span class="sxs-lookup"><span data-stu-id="da8d6-122">**static inline Init(D3D12\_ROOT\_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE)**</span></span>
</dt> <dd>

<span data-ttu-id="da8d6-123">Especifica uma função que inicializa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="da8d6-123">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="da8d6-124">[**D3D12 \_ Tabela \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) de &de DESCRIPTOR1 raiz</span><span class="sxs-lookup"><span data-stu-id="da8d6-124">[**D3D12\_ROOT\_DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &table</span></span>

<span data-ttu-id="da8d6-125">ShaderRegister UINT</span><span class="sxs-lookup"><span data-stu-id="da8d6-125">UINT shaderRegister</span></span>

<span data-ttu-id="da8d6-126">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="da8d6-126">UINT registerSpace = 0</span></span>

<span data-ttu-id="da8d6-127">[**D3D12 \_ Sinalizadores \_ de \_ sinalizadores de descritor de raiz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = \_ sinalizador de \_ descritor raiz D3D12 \_ \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="da8d6-127">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="da8d6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da8d6-128">Requirements</span></span>



| <span data-ttu-id="da8d6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="da8d6-129">Requirement</span></span> | <span data-ttu-id="da8d6-130">Valor</span><span class="sxs-lookup"><span data-stu-id="da8d6-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da8d6-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da8d6-131">Header</span></span><br/> | <dl> <span data-ttu-id="da8d6-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="da8d6-132"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da8d6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="da8d6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da8d6-134">**D3D12 \_ raiz \_ DESCRIPTOR1**</span><span class="sxs-lookup"><span data-stu-id="da8d6-134">**D3D12\_ROOT\_DESCRIPTOR1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[<span data-ttu-id="da8d6-135">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="da8d6-135">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





