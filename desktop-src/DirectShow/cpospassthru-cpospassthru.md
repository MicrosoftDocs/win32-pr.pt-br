---
description: Método de construtor.
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
ms.openlocfilehash: ba49bd1e2f65cf0d2a8a398ecab167e74dc35ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105766319"
---
# <a name="cpospassthrucpospassthru-constructor"></a><span data-ttu-id="12050-103">Construtor CPosPassThru. CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="12050-103">CPosPassThru.CPosPassThru constructor</span></span>

<span data-ttu-id="12050-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="12050-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12050-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12050-105">Syntax</span></span>


```C++
CPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin,
                   
);
```



## <a name="parameters"></a><span data-ttu-id="12050-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12050-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12050-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="12050-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="12050-108">Ponteiro para o nome do objeto, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="12050-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="12050-109">Aloque esse parâmetro na memória estática.</span><span class="sxs-lookup"><span data-stu-id="12050-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="12050-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="12050-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="12050-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="12050-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="12050-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="12050-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="12050-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="12050-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="12050-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="12050-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="12050-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="12050-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="12050-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="12050-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="12050-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="12050-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="12050-118">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN de entrada do filtro.</span><span class="sxs-lookup"><span data-stu-id="12050-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> <dt>

 
</dt> <dd></dd> </dl>

 

 



