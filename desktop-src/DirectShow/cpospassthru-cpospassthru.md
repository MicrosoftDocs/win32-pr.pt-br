---
description: Construtor de CPosPassThru. CPosPassThru-método de construtor.
ms.assetid: b258401c-158b-4eb8-8736-1e1ad9a8403a
title: Construtor CPosPassThru. CPosPassThru
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CPosPassThru
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a6c49b305b3c6638aeaaee1480d0b561fd8c99a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085594"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="03f36-103">Construtor CPosPassThru. CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="03f36-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="03f36-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="03f36-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f36-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03f36-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="03f36-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03f36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f36-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="03f36-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="03f36-108">Ponteiro para o nome do objeto, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="03f36-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="03f36-109">Aloque esse parâmetro na memória estática.</span><span class="sxs-lookup"><span data-stu-id="03f36-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="03f36-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="03f36-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="03f36-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="03f36-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="03f36-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="03f36-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="03f36-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="03f36-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="03f36-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="03f36-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="03f36-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03f36-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="03f36-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="03f36-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="03f36-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="03f36-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="03f36-118">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN de entrada do filtro.</span><span class="sxs-lookup"><span data-stu-id="03f36-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



