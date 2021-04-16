---
title: Estrutura de CD3DX12_CLEAR_VALUE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de valor claro D3D12 \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Estrutura de CD3DX12_CLEAR_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747664"
---
# <a name="cd3dx12_clear_value-structure"></a><span data-ttu-id="9ca8a-104">CD3DX12 \_ limpar \_ estrutura de valor</span><span class="sxs-lookup"><span data-stu-id="9ca8a-104">CD3DX12\_CLEAR\_VALUE structure</span></span>

<span data-ttu-id="9ca8a-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ valor claro D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .</span><span class="sxs-lookup"><span data-stu-id="9ca8a-105">A helper structure to enable easy initialization of a [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca8a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ca8a-106">Syntax</span></span>


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a><span data-ttu-id="9ca8a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9ca8a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ca8a-108">**CD3DX12 \_ limpar \_ valor ()**</span><span class="sxs-lookup"><span data-stu-id="9ca8a-108">**CD3DX12\_CLEAR\_VALUE()**</span></span>
</dt> <dd>

<span data-ttu-id="9ca8a-109">Cria uma nova instância, não inicializada, de um \_ valor de limpeza CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="9ca8a-109">Creates a new, uninitialized, instance of a CD3DX12\_CLEAR\_VALUE.</span></span>

</dd> <dt>

<span data-ttu-id="9ca8a-110">**\_valor de limpeza CD3DX12 explícito \_ (const D3D12 \_ limpar \_ valor &o)**</span><span class="sxs-lookup"><span data-stu-id="9ca8a-110">**explicit CD3DX12\_CLEAR\_VALUE(const D3D12\_CLEAR\_VALUE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="9ca8a-111">Cria uma nova instância de um valor de limpeza de CD3DX12 \_ \_ , inicializada com o conteúdo de outra estrutura de [**\_ \_ valor de limpeza D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .</span><span class="sxs-lookup"><span data-stu-id="9ca8a-111">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initialized with the contents of another [**D3D12\_CLEAR\_VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ca8a-112">**CD3DX12 \_ \_ valor de limpeza ( \_ formato de formato dxgi, cor de float de const \[ 4 \] )**</span><span class="sxs-lookup"><span data-stu-id="9ca8a-112">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, const FLOAT color\[ 4 \])**</span></span>
</dt> <dd>

<span data-ttu-id="9ca8a-113">Cria uma nova instância de um \_ valor de limpeza CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9ca8a-113">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="9ca8a-114">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="9ca8a-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="9ca8a-115">Cor de FLUTUAção \[ 4 \]</span><span class="sxs-lookup"><span data-stu-id="9ca8a-115">FLOAT color\[ 4 \]</span></span>

</dd> <dt>

<span data-ttu-id="9ca8a-116">**CD3DX12 \_ \_ valor de limpeza ( \_ formato de formato dxgi, profundidade flutuante, estêncil UINT8)**</span><span class="sxs-lookup"><span data-stu-id="9ca8a-116">**CD3DX12\_CLEAR\_VALUE(DXGI\_FORMAT format, FLOAT depth, UINT8 stencil)**</span></span>
</dt> <dd>

<span data-ttu-id="9ca8a-117">Cria uma nova instância de um \_ valor de limpeza CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9ca8a-117">Creates a new instance of a CD3DX12\_CLEAR\_VALUE, initializing the following parameters:</span></span>

<span data-ttu-id="9ca8a-118">[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato</span><span class="sxs-lookup"><span data-stu-id="9ca8a-118">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="9ca8a-119">Profundidade de FLUTUAção</span><span class="sxs-lookup"><span data-stu-id="9ca8a-119">FLOAT depth</span></span>

<span data-ttu-id="9ca8a-120">Estêncil UINT8</span><span class="sxs-lookup"><span data-stu-id="9ca8a-120">UINT8 stencil</span></span>

</dd> <dt>

<span data-ttu-id="9ca8a-121">**const D3D12 do operador const \_ \_ de valor limpo& () constante**</span><span class="sxs-lookup"><span data-stu-id="9ca8a-121">**operator const D3D12\_CLEAR\_VALUE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="9ca8a-122">Define o & operador de passagem por referência para o tipo de estrutura pai.</span><span class="sxs-lookup"><span data-stu-id="9ca8a-122">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ca8a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ca8a-123">Requirements</span></span>



| <span data-ttu-id="9ca8a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ca8a-124">Requirement</span></span> | <span data-ttu-id="9ca8a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9ca8a-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca8a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ca8a-126">Header</span></span><br/> | <dl> <span data-ttu-id="9ca8a-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ca8a-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ca8a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ca8a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca8a-129">**D3D12 \_ limpar \_ valor**</span><span class="sxs-lookup"><span data-stu-id="9ca8a-129">**D3D12\_CLEAR\_VALUE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[<span data-ttu-id="9ca8a-130">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="9ca8a-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

