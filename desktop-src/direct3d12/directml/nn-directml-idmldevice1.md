---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Representa um dispositivo DirectML, que é usado para criar operadores, tabelas de associação, gravadores de comandos e outros objetos.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803743"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="7d6d7-103">Interface IDMLDevice1 (directml. h)</span><span class="sxs-lookup"><span data-stu-id="7d6d7-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="7d6d7-104">Representa um dispositivo DirectML, que é usado para criar operadores, tabelas de associação, gravadores de comandos e outros objetos.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="7d6d7-105">A interface **IDMLDevice1** herda de [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span><span class="sxs-lookup"><span data-stu-id="7d6d7-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="7d6d7-106">Um dispositivo DirectML sempre está associado a exatamente um dispositivo Direct3D 12 subjacente.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="7d6d7-107">Todos os objetos criados pelo dispositivo DirectML mantêm uma referência forte para seu dispositivo pai.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="7d6d7-108">Ao contrário do dispositivo Direct3D 12, o dispositivo DML não é um singleton.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="7d6d7-109">Portanto, é possível criar vários dispositivos DirectML no mesmo dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="7d6d7-110">No entanto, isso não é recomendado, pois o dispositivo DirectML não tem um estado mutável, portanto, há pouca vantagem em criar vários dispositivos DML no mesmo dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="7d6d7-111">Esse objeto é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d6d7-112">Essa API está disponível como parte do pacote redistribuível DirectML autônomo (consulte [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versão 1,4 e posterior.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="7d6d7-113">Consulte também o [histórico de versão do DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="7d6d7-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="7d6d7-114">Disponibilidade</span><span class="sxs-lookup"><span data-stu-id="7d6d7-114">Availability</span></span>
<span data-ttu-id="7d6d7-115">Essa API foi introduzida na versão DirectML `1.1.0` .</span><span class="sxs-lookup"><span data-stu-id="7d6d7-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="7d6d7-116">Restrições de tensor</span><span class="sxs-lookup"><span data-stu-id="7d6d7-116">Tensor constraints</span></span>
<span data-ttu-id="7d6d7-117">**Plataforma de destino**: Windows</span><span class="sxs-lookup"><span data-stu-id="7d6d7-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="7d6d7-118">Herança</span><span class="sxs-lookup"><span data-stu-id="7d6d7-118">Inheritance</span></span>


<span data-ttu-id="7d6d7-119">A interface IDMLDevice1 herda da interface IDMLDevice.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="7d6d7-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="7d6d7-120">Methods</span></span>

<p><span data-ttu-id="7d6d7-121">A interface <b>IDMLDevice1</b> tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="7d6d7-122">Método</span><span class="sxs-lookup"><span data-stu-id="7d6d7-122">Method</span></span> | <span data-ttu-id="7d6d7-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d6d7-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="7d6d7-124">IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="7d6d7-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="7d6d7-125">Compila um grafo de operadores DirectML em um objeto que pode ser expedido para a GPU.</span><span class="sxs-lookup"><span data-stu-id="7d6d7-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="7d6d7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d6d7-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7d6d7-127">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="7d6d7-127">**Target Platform**</span></span> | <span data-ttu-id="7d6d7-128">Windows</span><span class="sxs-lookup"><span data-stu-id="7d6d7-128">Windows</span></span> |
| <span data-ttu-id="7d6d7-129">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="7d6d7-129">**Header**</span></span> | <span data-ttu-id="7d6d7-130">directml. h</span><span class="sxs-lookup"><span data-stu-id="7d6d7-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="7d6d7-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d6d7-131">See also</span></span>

[<span data-ttu-id="7d6d7-132">Interface IDMLDevice</span><span class="sxs-lookup"><span data-stu-id="7d6d7-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)