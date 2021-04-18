---
description: Se um evento estiver disponível, o método NextEvent do objeto SWbemEventSource recuperará o evento de uma consulta de evento.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Método SWbemEventSource. NextEvent (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764439"
---
# <a name="swbemeventsourcenextevent-method"></a><span data-ttu-id="f1911-103">Método SWbemEventSource. NextEvent</span><span class="sxs-lookup"><span data-stu-id="f1911-103">SWbemEventSource.NextEvent method</span></span>

<span data-ttu-id="f1911-104">Se um evento estiver disponível, o método **NextEvent** do objeto [**SWbemEventSource**](swbemeventsource.md) recuperará o evento de uma consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="f1911-104">If an event is available, the **NextEvent** method of the [**SWbemEventSource**](swbemeventsource.md) object retrieves the event from an event query.</span></span>

<span data-ttu-id="f1911-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f1911-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1911-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1911-106">Syntax</span></span>


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f1911-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1911-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1911-108">*iTimeoutMs* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f1911-108">*iTimeoutMs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1911-109">Número de milissegundos durante os quais a chamada aguarda um evento antes de retornar um erro de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="f1911-109">Number of milliseconds the call waits for an event before returning a time-out error.</span></span> <span data-ttu-id="f1911-110">O valor padrão para esse parâmetro é **wbemTimeoutInfinite** (-1), que direciona a chamada para aguardar indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="f1911-110">The default value for this parameter is **wbemTimeoutInfinite** (-1), which directs the call to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1911-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1911-111">Return value</span></span>

<span data-ttu-id="f1911-112">Se o método **NextEvent** for bem-sucedido, ele retornará um objeto [**SWbemObject**](swbemobject.md) que contém o evento solicitado.</span><span class="sxs-lookup"><span data-stu-id="f1911-112">If the **NextEvent** method is successful, it returns an [**SWbemObject**](swbemobject.md) object that contains the requested event.</span></span> <span data-ttu-id="f1911-113">Se a chamada atingir o tempo limite, o objeto retornado será **nulo** e um erro será gerado.</span><span class="sxs-lookup"><span data-stu-id="f1911-113">If the call times out, the returned object is **NULL** and an error is raised.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f1911-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f1911-114">Error codes</span></span>

<span data-ttu-id="f1911-115">Após a conclusão do método **NextEvent** , o objeto **Err** pode conter o código de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1911-115">Upon the completion of the **NextEvent** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f1911-116">**wbemErrTimedOut** -0x80043001</span><span class="sxs-lookup"><span data-stu-id="f1911-116">**wbemErrTimedOut** - 0x80043001</span></span>
</dt> <dd>

<span data-ttu-id="f1911-117">O evento solicitado não chegou no período de tempo especificado em *iTimeoutMs.*</span><span class="sxs-lookup"><span data-stu-id="f1911-117">Requested event did not arrive in the amount of time specified in *iTimeoutMs.*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1911-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1911-118">Requirements</span></span>



| <span data-ttu-id="f1911-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1911-119">Requirement</span></span> | <span data-ttu-id="f1911-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f1911-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1911-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1911-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1911-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1911-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1911-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1911-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1911-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1911-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1911-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1911-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1911-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1911-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1911-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f1911-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="f1911-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f1911-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f1911-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f1911-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1911-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1911-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f1911-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="f1911-131">CLSID</span></span><br/>                    | <span data-ttu-id="f1911-132">\_SWBEMEVENTSOURCE CLSID</span><span class="sxs-lookup"><span data-stu-id="f1911-132">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="f1911-133">IID</span><span class="sxs-lookup"><span data-stu-id="f1911-133">IID</span></span><br/>                      | <span data-ttu-id="f1911-134">ISWbemEventSource de IID \_</span><span class="sxs-lookup"><span data-stu-id="f1911-134">IID\_ISWbemEventSource</span></span><br/>                                                       |



 

 




