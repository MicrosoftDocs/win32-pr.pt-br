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
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638419"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="56437-105">D1102: muitos identificadores abertos</span><span class="sxs-lookup"><span data-stu-id="56437-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="56437-106">Um grande número de interfaces não lançadas foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="56437-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="56437-107">Atualmente, há um \[ *número* \] de interfaces não lançadas alocadas por essa dll.</span><span class="sxs-lookup"><span data-stu-id="56437-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="56437-108">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="56437-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="56437-109"><span id="number"></span><span id="NUMBER"></span>*automática*</span><span class="sxs-lookup"><span data-stu-id="56437-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="56437-110">O número de interfaces não lançadas alocadas por essa DLL.</span><span class="sxs-lookup"><span data-stu-id="56437-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="56437-111">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="56437-111">Error Level</span></span> | <span data-ttu-id="56437-112">Aviso</span><span class="sxs-lookup"><span data-stu-id="56437-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="56437-113">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="56437-113">Possible Causes</span></span>

<span data-ttu-id="56437-114">Um grande número de recursos foi criado.</span><span class="sxs-lookup"><span data-stu-id="56437-114">A large number of resources were created.</span></span> <span data-ttu-id="56437-115">Embora Direct2D não tenha limite superior no número de recursos disponíveis (exceto memória), a camada de depuração emite essa mensagem informativa quando encontra 1001 objetos dinâmicos, 2001 objetos dinâmicos ou 3001 objetos dinâmicos etc, porque isso pode indicar um vazamento no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="56437-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




