---
description: O evento OnObjectPut de um objeto SWbemSink é disparado quando uma operação Put assíncrona é concluída. Esse evento retorna o caminho do objeto da instância ou da classe salva.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectPut (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171968"
---
# <a name="iswbemsinkeventsonobjectput-event"></a><span data-ttu-id="7b389-104">Evento ISWbemSinkEvents:: OnObjectPut</span><span class="sxs-lookup"><span data-stu-id="7b389-104">ISWbemSinkEvents::OnObjectPut event</span></span>

<span data-ttu-id="7b389-105">O evento **OnObjectPut** de um objeto [**SWbemSink**](swbemsink.md) é disparado quando uma operação Put assíncrona é concluída.</span><span class="sxs-lookup"><span data-stu-id="7b389-105">The **OnObjectPut** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous Put operation is complete.</span></span> <span data-ttu-id="7b389-106">Esse evento retorna o caminho do objeto da instância ou da classe salva.</span><span class="sxs-lookup"><span data-stu-id="7b389-106">This event returns the object path of the instance or the saved class.</span></span>

<span data-ttu-id="7b389-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7b389-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b389-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b389-108">Syntax</span></span>


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="7b389-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b389-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b389-110">*objWbemObjectPath*</span><span class="sxs-lookup"><span data-stu-id="7b389-110">*objWbemObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="7b389-111">Um objeto [**SWbemObjectPath**](swbemobjectpath.md) , que contém o caminho do objeto da instância ou classe que a operação Put grava no WMI.</span><span class="sxs-lookup"><span data-stu-id="7b389-111">An [**SWbemObjectPath**](swbemobjectpath.md) object, that contains the object path of the instance or class that the put operation writes to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="7b389-112">*objWbemAsyncContext*</span><span class="sxs-lookup"><span data-stu-id="7b389-112">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="7b389-113">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é passado para a chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="7b389-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="7b389-114">Use esse parâmetro para identificar a origem da chamada assíncrona que dispara esse evento quando várias chamadas assíncronas são feitas usando esse coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="7b389-114">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b389-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b389-115">Return value</span></span>

<span data-ttu-id="7b389-116">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7b389-116">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b389-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7b389-117">Error codes</span></span>

<span data-ttu-id="7b389-118">Após a conclusão do evento **OnObjectPut** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="7b389-118">After the completion of the **OnObjectPut** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="7b389-119">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7b389-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7b389-120">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="7b389-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7b389-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7b389-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7b389-122">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="7b389-122">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7b389-123">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="7b389-123">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="7b389-124">Ocorreu um erro de rede, impedindo a operação normal.</span><span class="sxs-lookup"><span data-stu-id="7b389-124">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b389-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b389-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7b389-126">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="7b389-126">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="7b389-127">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7b389-127">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="7b389-128">Para eliminar os riscos, use a comunicação semi-síncrona ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="7b389-128">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="7b389-129">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7b389-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b389-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b389-130">Requirements</span></span>



| <span data-ttu-id="7b389-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b389-131">Requirement</span></span> | <span data-ttu-id="7b389-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7b389-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b389-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b389-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7b389-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b389-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b389-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b389-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7b389-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b389-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b389-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7b389-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b389-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b389-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b389-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="7b389-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b389-140"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b389-140"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7b389-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7b389-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b389-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b389-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7b389-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="7b389-143">CLSID</span></span><br/>                    | <span data-ttu-id="7b389-144">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="7b389-144">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="7b389-145">IID</span><span class="sxs-lookup"><span data-stu-id="7b389-145">IID</span></span><br/>                      | <span data-ttu-id="7b389-146">ISWbemSinkEvents de IID \_</span><span class="sxs-lookup"><span data-stu-id="7b389-146">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="7b389-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b389-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b389-148">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="7b389-148">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

