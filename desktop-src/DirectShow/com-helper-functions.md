---
description: Essas funções fornecem suporte para implementar a interface IUnknown no DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Funções auxiliares COM (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754260"
---
# <a name="com-helper-functions"></a><span data-ttu-id="f4979-103">Funções auxiliares COM</span><span class="sxs-lookup"><span data-stu-id="f4979-103">COM Helper Functions</span></span>

<span data-ttu-id="f4979-104">Essas funções fornecem suporte para implementar a interface **IUnknown** no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f4979-104">These functions provide support for implementing the **IUnknown** interface in DirectShow.</span></span>



| <span data-ttu-id="f4979-105">Função</span><span class="sxs-lookup"><span data-stu-id="f4979-105">Function</span></span>                                               | <span data-ttu-id="f4979-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4979-106">Description</span></span>                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="f4979-107">**DECLARAR \_ IUnknown**</span><span class="sxs-lookup"><span data-stu-id="f4979-107">**DECLARE\_IUNKNOWN**</span></span>](declare-iunknown.md)          | <span data-ttu-id="f4979-108">Declara os três métodos da interface base para uma nova interface.</span><span class="sxs-lookup"><span data-stu-id="f4979-108">Declares the three methods of the base interface for a new interface.</span></span> |
| [<span data-ttu-id="f4979-109">**GetInterface**</span><span class="sxs-lookup"><span data-stu-id="f4979-109">**GetInterface**</span></span>](getinterface.md)                   | <span data-ttu-id="f4979-110">Recupera um ponteiro de interface para o cliente solicitado.</span><span class="sxs-lookup"><span data-stu-id="f4979-110">Retrieves an interface pointer to the requested client.</span></span>               |
| [<span data-ttu-id="f4979-111">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="f4979-111">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md) | <span data-ttu-id="f4979-112">Versão não delegada da interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="f4979-112">Nondelegating version of the **IUnknown** interface.</span></span>                  |
| [<span data-ttu-id="f4979-113">**LoadOLEAut32**</span><span class="sxs-lookup"><span data-stu-id="f4979-113">**LoadOLEAut32**</span></span>](loadoleaut32.md)                   | <span data-ttu-id="f4979-114">Carrega a DLL de automação (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="f4979-114">Loads the Automation DLL (OleAut32.dll).</span></span>                              |



 

## <a name="requirements"></a><span data-ttu-id="f4979-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4979-115">Requirements</span></span>



| <span data-ttu-id="f4979-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4979-116">Requirement</span></span> | <span data-ttu-id="f4979-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f4979-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4979-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4979-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f4979-119"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4979-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f4979-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4979-120">Library</span></span><br/> | <dl> <span data-ttu-id="f4979-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f4979-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4979-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4979-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4979-123">Funções de utilitário</span><span class="sxs-lookup"><span data-stu-id="f4979-123">Utility Functions</span></span>](utility-functions.md)
</dt> </dl>

 

 




