---
title: Função CommandListCast (D3dx12. h)
description: Esse modelo de função converte um ponteiro constante para qualquer lista de comandos em um ponteiro const para um ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- Função CommandListCast
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772504"
---
# <a name="commandlistcast-function"></a><span data-ttu-id="d5804-104">Função CommandListCast</span><span class="sxs-lookup"><span data-stu-id="d5804-104">CommandListCast function</span></span>

<span data-ttu-id="d5804-105">Esse modelo de função converte um ponteiro constante para qualquer lista de comandos em um ponteiro const para um ID3D12CommandList.</span><span class="sxs-lookup"><span data-stu-id="d5804-105">This function template casts a constant pointer to any command list into a const pointer to an ID3D12CommandList.</span></span>

<span data-ttu-id="d5804-106">Essa conversão é útil para passar ponteiros de lista de comandos fortemente tipados para o [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="d5804-106">This cast is useful for passing strongly-typed command list pointers into [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5804-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5804-107">Syntax</span></span>


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a><span data-ttu-id="d5804-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5804-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5804-109">*PP*</span><span class="sxs-lookup"><span data-stu-id="d5804-109">*pp*</span></span> 
</dt> <dd>

<span data-ttu-id="d5804-110">Tipo: **t \_ CommandListType \* const \***</span><span class="sxs-lookup"><span data-stu-id="d5804-110">Type: **t\_CommandListType \* const \***</span></span>

<span data-ttu-id="d5804-111">A lista de comandos fortemente tipados a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="d5804-111">The strongly-typed command list to cast.</span></span>

<span data-ttu-id="d5804-112">O argumento de modelo **t \_ CommandListType** Especifica qualquer objeto de lista de comandos fortemente tipados.</span><span class="sxs-lookup"><span data-stu-id="d5804-112">The template argument **t\_CommandListType** specifies any strongly-typed command list object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5804-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5804-113">Return value</span></span>

<span data-ttu-id="d5804-114">Tipo: **ID3D12CommandList \* const \***</span><span class="sxs-lookup"><span data-stu-id="d5804-114">Type: **ID3D12CommandList \* const \***</span></span>

<span data-ttu-id="d5804-115">A lista de comandos com rigidez de tipos, reinterpreta como um [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span><span class="sxs-lookup"><span data-stu-id="d5804-115">The strongly-typed command list, reinterpreted as an [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5804-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5804-116">Remarks</span></span>

<span data-ttu-id="d5804-117">CommandListCast executa uma **\_ conversão de reinterpretação**.</span><span class="sxs-lookup"><span data-stu-id="d5804-117">CommandListCast performs a **reinterpret\_cast**.</span></span> <span data-ttu-id="d5804-118">A conversão é válida, contanto que const-qualidade da lista de comandos seja respeitado.</span><span class="sxs-lookup"><span data-stu-id="d5804-118">The cast is valid as long as the const-ness of the command list is respected.</span></span>

<span data-ttu-id="d5804-119">A função CommandListCast é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d5804-119">The CommandListCast function is defined as the following:</span></span>


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a><span data-ttu-id="d5804-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5804-120">Requirements</span></span>



| <span data-ttu-id="d5804-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5804-121">Requirement</span></span> | <span data-ttu-id="d5804-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d5804-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d5804-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5804-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d5804-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5804-124"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="d5804-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5804-125">Library</span></span><br/> | <dl> <span data-ttu-id="d5804-126"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5804-126"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="d5804-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d5804-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="d5804-128"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5804-128"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5804-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5804-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5804-130">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="d5804-130">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





