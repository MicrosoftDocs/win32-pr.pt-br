---
title: Método de back IWMPDVD
description: O método back altera a exibição de um submenu para seu menu pai.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- método de back Windows Media Player
- método de back Windows Media Player, interface IWMPDVD
- Interface IWMPDVD Windows Media Player, método back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755459"
---
# <a name="iwmpdvdback-method"></a><span data-ttu-id="5be77-106">Método IWMPDVD:: back</span><span class="sxs-lookup"><span data-stu-id="5be77-106">IWMPDVD::back method</span></span>

<span data-ttu-id="5be77-107">O método **back** altera a exibição de um submenu para seu menu pai.</span><span class="sxs-lookup"><span data-stu-id="5be77-107">The **back** method changes the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be77-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5be77-108">Syntax</span></span>


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a><span data-ttu-id="5be77-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5be77-109">Parameters</span></span>

<span data-ttu-id="5be77-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5be77-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5be77-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5be77-111">Return value</span></span>

<span data-ttu-id="5be77-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5be77-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5be77-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5be77-113">Remarks</span></span>

<span data-ttu-id="5be77-114">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="5be77-114">Every DVD is authored differently.</span></span> <span data-ttu-id="5be77-115">Alguns DVDs são criados para que o `back` método esteja disponível no menu raiz, mas quando invocado, ele não fará nada.</span><span class="sxs-lookup"><span data-stu-id="5be77-115">Some DVDs are authored so that the `back` method is available from the root menu, but when invoked, it will do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5be77-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5be77-116">Requirements</span></span>



| <span data-ttu-id="5be77-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5be77-117">Requirement</span></span> | <span data-ttu-id="5be77-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5be77-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5be77-119">Versão</span><span class="sxs-lookup"><span data-stu-id="5be77-119">Version</span></span><br/>   | <span data-ttu-id="5be77-120">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="5be77-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5be77-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="5be77-121">Namespace</span></span><br/> | <span data-ttu-id="5be77-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5be77-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5be77-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="5be77-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5be77-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5be77-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5be77-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5be77-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be77-126">**Interface IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5be77-126">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





