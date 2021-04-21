---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila um grafo de operadores DirectML em um objeto que pode ser expedido para a GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803745"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="05496-103">Método IDMLDevice1:: CompileGraph (directml. h)</span><span class="sxs-lookup"><span data-stu-id="05496-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="05496-104">Compila um grafo de operadores DirectML em um objeto que pode ser expedido para a GPU.</span><span class="sxs-lookup"><span data-stu-id="05496-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="05496-105">Um operador compilado representa a forma de inclusas eficiente de um operador adequado para execução na GPU.</span><span class="sxs-lookup"><span data-stu-id="05496-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="05496-106">Um operador compilado mantém o estado (como sombreadores e outros objetos) necessários para a execução.</span><span class="sxs-lookup"><span data-stu-id="05496-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="05496-107">Como um operador compilado implementa a interface [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) , você poderá remover uma da memória GPU, se desejar.</span><span class="sxs-lookup"><span data-stu-id="05496-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="05496-108">Consulte [IDMLDevice1:: Remove](/windows/win32/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice1:: MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="05496-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="05496-109">O operador Compiled não usa nem referencia os objetos [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) fornecidos na descrição do grafo depois que esse método retorna.</span><span class="sxs-lookup"><span data-stu-id="05496-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05496-110">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="05496-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="05496-111">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="05496-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="05496-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05496-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="05496-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05496-113">Parameters</span></span>

`desc`

<span data-ttu-id="05496-114">Tipo: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="05496-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="05496-115">Uma descrição do grafo a ser compilado.</span><span class="sxs-lookup"><span data-stu-id="05496-115">A description of the graph to compile.</span></span> <span data-ttu-id="05496-116">Consulte [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span><span class="sxs-lookup"><span data-stu-id="05496-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="05496-117">Tipo: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="05496-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="05496-118">Todos os sinalizadores para controlar a execução desse operador.</span><span class="sxs-lookup"><span data-stu-id="05496-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="05496-119">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="05496-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="05496-120">Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em <i>PPV</i>.</span><span class="sxs-lookup"><span data-stu-id="05496-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="05496-121">Espera-se que seja o GUID de [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span><span class="sxs-lookup"><span data-stu-id="05496-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="05496-122">Tipo: <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="05496-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="05496-123">Um ponteiro para um bloco de memória que recebe um ponteiro para o operador compilado.</span><span class="sxs-lookup"><span data-stu-id="05496-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="05496-124">Esse é o endereço de um ponteiro para um [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representando o operador compilado criado.</span><span class="sxs-lookup"><span data-stu-id="05496-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="05496-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05496-125">Return value</span></span>

<span data-ttu-id="05496-126">Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="05496-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="05496-127">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="05496-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="05496-128">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05496-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="05496-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="05496-129">Remarks</span></span>

<span data-ttu-id="05496-130">A API de grafo do operador DirectML fornece uma maneira abstrata de usar o DirectML de forma eficiente em diversos hardwares.</span><span class="sxs-lookup"><span data-stu-id="05496-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="05496-131">O DirectML aplica otimizações de nível de tensor, como escolher o layout de tensor mais eficiente com base no adaptador que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="05496-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="05496-132">Ele também aplica otimizações como a remoção de operadores de junção ou de divisão.</span><span class="sxs-lookup"><span data-stu-id="05496-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="05496-133">Recomendamos que você aplique otimizações de alto nível antes de criar um grafo DirectML.</span><span class="sxs-lookup"><span data-stu-id="05496-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="05496-134">Por exemplo, a mistura de operadores de convolução com BatchNorm, dobramento de constantes e eliminação de subexpressão comum.</span><span class="sxs-lookup"><span data-stu-id="05496-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="05496-135">As otimizações no otimizador de grafo do DirectML são destinadas a complementar tais otimizações independentes de dispositivo, que geralmente são tratadas genericamente pelas estruturas do Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="05496-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="05496-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05496-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="05496-137">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="05496-137">**Target Platform**</span></span> | <span data-ttu-id="05496-138">Windows</span><span class="sxs-lookup"><span data-stu-id="05496-138">Windows</span></span> |
| <span data-ttu-id="05496-139">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="05496-139">**Header**</span></span> | <span data-ttu-id="05496-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="05496-140">directml.h</span></span> |
| <span data-ttu-id="05496-141">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="05496-141">**Library**</span></span> | <span data-ttu-id="05496-142">DirectML. lib</span><span class="sxs-lookup"><span data-stu-id="05496-142">DirectML.lib</span></span> |
| <span data-ttu-id="05496-143">**DLL**</span><span class="sxs-lookup"><span data-stu-id="05496-143">**DLL**</span></span> | <span data-ttu-id="05496-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="05496-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="05496-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="05496-145">See also</span></span>

[<span data-ttu-id="05496-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="05496-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)