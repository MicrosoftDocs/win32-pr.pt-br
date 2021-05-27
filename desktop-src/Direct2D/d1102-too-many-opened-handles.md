---
title: D1102 um número excessivo de identificadores abertos
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Um grande número de interfaces não lançadas foi encontrado. Atualmente, há interfaces não lançadas alocadas por essa DLL.
keywords:
- D1102 um número excessivo de identificadores abertos Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548681"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="c7854-105">D1102: muitos identificadores abertos</span><span class="sxs-lookup"><span data-stu-id="c7854-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="c7854-106">Um grande número de interfaces não lançadas foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="c7854-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="c7854-107">Atualmente, há um \[ *número* \] de interfaces não lançadas alocadas por essa dll.</span><span class="sxs-lookup"><span data-stu-id="c7854-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="c7854-108">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="c7854-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="c7854-109"><span id="number"></span><span id="NUMBER"></span>*automática*</span><span class="sxs-lookup"><span data-stu-id="c7854-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="c7854-110">O número de interfaces não lançadas alocadas por essa DLL.</span><span class="sxs-lookup"><span data-stu-id="c7854-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| <span data-ttu-id="c7854-111">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="c7854-111">Error Level</span></span> | <span data-ttu-id="c7854-112">Aviso</span><span class="sxs-lookup"><span data-stu-id="c7854-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="c7854-113">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="c7854-113">Possible Causes</span></span>

<span data-ttu-id="c7854-114">Um grande número de recursos foi criado.</span><span class="sxs-lookup"><span data-stu-id="c7854-114">A large number of resources were created.</span></span> <span data-ttu-id="c7854-115">Embora Direct2D não tenha limite superior no número de recursos disponíveis (exceto memória), a camada de depuração emite essa mensagem informativa quando encontra 1001 objetos dinâmicos, 2001 objetos dinâmicos ou 3001 objetos dinâmicos etc, porque isso pode indicar um vazamento no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c7854-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




