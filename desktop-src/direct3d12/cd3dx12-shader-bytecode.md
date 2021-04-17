---
title: Estrutura de CD3DX12_SHADER_BYTECODE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de código de bytes do sombreador D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Estrutura de CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765356"
---
# <a name="cd3dx12_shader_bytecode-structure"></a><span data-ttu-id="2366c-104">\_Estrutura de código de bytes do sombreador CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="2366c-104">CD3DX12\_SHADER\_BYTECODE structure</span></span>

<span data-ttu-id="2366c-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ código de \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="2366c-105">A helper structure to enable easy initialization of a [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2366c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2366c-106">Syntax</span></span>


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a><span data-ttu-id="2366c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2366c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2366c-108">**\_ \_ Código de bytes do sombreador CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="2366c-108">**CD3DX12\_SHADER\_BYTECODE()**</span></span>
</dt> <dd>

<span data-ttu-id="2366c-109">Cria uma nova instância, não inicializada, de um \_ código de bytes do sombreador CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="2366c-109">Creates a new, uninitialized, instance of a CD3DX12\_SHADER\_BYTECODE.</span></span>

</dd> <dt>

<span data-ttu-id="2366c-110">**\_ \_ código de bytes CD3DX12 do sombreador explícito (const D3D12 do \_ sombreador de \_ bytes &o)**</span><span class="sxs-lookup"><span data-stu-id="2366c-110">**explicit CD3DX12\_SHADER\_BYTECODE(const D3D12\_SHADER\_BYTECODE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="2366c-111">Cria uma nova instância de um \_ código de bytes do sombreador CD3DX12 \_ , inicializado com o conteúdo de outra estrutura de [**código de \_ \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .</span><span class="sxs-lookup"><span data-stu-id="2366c-111">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initialized with the contents of another [**D3D12\_SHADER\_BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2366c-112">**\_ \_ Código de bytes do sombreador CD3DX12 (ID3DBlob \* pShaderBlob)**</span><span class="sxs-lookup"><span data-stu-id="2366c-112">**CD3DX12\_SHADER\_BYTECODE(ID3DBlob\* pShaderBlob)**</span></span>
</dt> <dd>

<span data-ttu-id="2366c-113">Cria uma nova instância de um \_ código de bytes do sombreador CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="2366c-113">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="2366c-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob</span><span class="sxs-lookup"><span data-stu-id="2366c-114">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))\* pShaderBlob</span></span>

</dd> <dt>

<span data-ttu-id="2366c-115">**\_ \_ Código de bytes do sombreador CD3DX12 (const void \* \_ PShaderBytecode, Size \_ T bytecodeLength)**</span><span class="sxs-lookup"><span data-stu-id="2366c-115">**CD3DX12\_SHADER\_BYTECODE(const void\* \_pShaderBytecode, SIZE\_T bytecodeLength)**</span></span>
</dt> <dd>

<span data-ttu-id="2366c-116">Cria uma nova instância de um \_ código de bytes do sombreador CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="2366c-116">Creates a new instance of a CD3DX12\_SHADER\_BYTECODE, initializing the following parameters:</span></span>

<span data-ttu-id="2366c-117">anular \* \_ pShaderBytecode</span><span class="sxs-lookup"><span data-stu-id="2366c-117">void\* \_pShaderBytecode</span></span>

<span data-ttu-id="2366c-118">DIMENSIONAR \_ T bytecodeLength</span><span class="sxs-lookup"><span data-stu-id="2366c-118">SIZE\_T bytecodeLength</span></span>

</dd> <dt>

<span data-ttu-id="2366c-119">**\_ \_ constante de D3D12 de código de bytes de sombreador const a& () const**</span><span class="sxs-lookup"><span data-stu-id="2366c-119">**operator const D3D12\_SHADER\_BYTECODE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="2366c-120">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="2366c-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2366c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2366c-121">Requirements</span></span>



| <span data-ttu-id="2366c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2366c-122">Requirement</span></span> | <span data-ttu-id="2366c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2366c-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2366c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2366c-124">Header</span></span><br/> | <dl> <span data-ttu-id="2366c-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="2366c-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2366c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2366c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2366c-127">**\_Código de bytes do sombreador D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="2366c-127">**D3D12\_SHADER\_BYTECODE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[<span data-ttu-id="2366c-128">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="2366c-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

