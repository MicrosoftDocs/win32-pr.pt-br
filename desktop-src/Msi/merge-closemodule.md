---
description: O método CloseModule do objeto de mesclagem fecha o módulo de mesclagem Windows Installer aberto no momento.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Método Merge. CloseModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780952"
---
# <a name="mergeclosemodule-method"></a><span data-ttu-id="e96e9-103">Método Merge. CloseModule</span><span class="sxs-lookup"><span data-stu-id="e96e9-103">Merge.CloseModule method</span></span>

<span data-ttu-id="e96e9-104">O método **CloseModule** do objeto de [**mesclagem**](merge-object.md) fecha o módulo de mesclagem Windows Installer aberto no momento.</span><span class="sxs-lookup"><span data-stu-id="e96e9-104">The **CloseModule** method of the [**Merge**](merge-object.md) object closes the currently open Windows Installer merge module.</span></span>

## <a name="syntax"></a><span data-ttu-id="e96e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e96e9-105">Syntax</span></span>


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a><span data-ttu-id="e96e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e96e9-106">Parameters</span></span>

<span data-ttu-id="e96e9-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e96e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e96e9-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e96e9-108">Return value</span></span>

<span data-ttu-id="e96e9-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e96e9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e96e9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e96e9-110">Remarks</span></span>

<span data-ttu-id="e96e9-111">Fechar um módulo de mesclagem não afetará nenhum erro que não tenha sido recuperado.</span><span class="sxs-lookup"><span data-stu-id="e96e9-111">Closing a merge module will not affect any errors that have not been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="e96e9-112">C++</span><span class="sxs-lookup"><span data-stu-id="e96e9-112">C++</span></span>

<span data-ttu-id="e96e9-113">Consulte a função [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .</span><span class="sxs-lookup"><span data-stu-id="e96e9-113">See [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e96e9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e96e9-114">Requirements</span></span>



| <span data-ttu-id="e96e9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e96e9-115">Requirement</span></span> | <span data-ttu-id="e96e9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e96e9-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e96e9-117">Versão</span><span class="sxs-lookup"><span data-stu-id="e96e9-117">Version</span></span><br/> | <span data-ttu-id="e96e9-118">Mergemod.dll 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e96e9-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="e96e9-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e96e9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e96e9-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e96e9-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="e96e9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e96e9-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e96e9-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e96e9-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
