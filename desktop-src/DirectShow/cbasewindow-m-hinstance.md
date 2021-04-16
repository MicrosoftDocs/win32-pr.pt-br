---
description: Identificador para a instância do módulo.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Membro CBaseWindow:: m_hInstance (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751254"
---
# <a name="cbasewindowm_hinstance-member"></a><span data-ttu-id="43e47-103">Membro de CBaseWindow:: m \_ HINSTANCE</span><span class="sxs-lookup"><span data-stu-id="43e47-103">CBaseWindow::m\_hInstance member</span></span>

<span data-ttu-id="43e47-104">Identificador para a instância do módulo.</span><span class="sxs-lookup"><span data-stu-id="43e47-104">Handle to the module instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e47-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43e47-105">Syntax</span></span>


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a><span data-ttu-id="43e47-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="43e47-106">Remarks</span></span>

<span data-ttu-id="43e47-107">A função de ponto de entrada de DLL define uma variável global com um identificador para a instância do módulo.</span><span class="sxs-lookup"><span data-stu-id="43e47-107">The DLL entry point function sets a global variable with a handle to the module instance.</span></span> <span data-ttu-id="43e47-108">A classe **CBaseWindow** armazena esse identificador em seu método construtor.</span><span class="sxs-lookup"><span data-stu-id="43e47-108">The **CBaseWindow** class stores this handle in its constructor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e47-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e47-109">Requirements</span></span>



| <span data-ttu-id="43e47-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e47-110">Requirement</span></span> | <span data-ttu-id="43e47-111">Valor</span><span class="sxs-lookup"><span data-stu-id="43e47-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43e47-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43e47-112">Header</span></span><br/>  | <dl> <span data-ttu-id="43e47-113"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43e47-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43e47-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43e47-114">Library</span></span><br/> | <dl> <span data-ttu-id="43e47-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="43e47-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43e47-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="43e47-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e47-117">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="43e47-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




