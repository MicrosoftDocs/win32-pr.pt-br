---
description: O método Cancel do objeto SWbemSink cancela todas as operações assíncronas pendentes associadas a esse coletor de objeto.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'Método ISWbemSink:: Cancel (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171969"
---
# <a name="iswbemsinkcancel-method"></a><span data-ttu-id="5b524-103">Método ISWbemSink:: Cancel</span><span class="sxs-lookup"><span data-stu-id="5b524-103">ISWbemSink::Cancel method</span></span>

<span data-ttu-id="5b524-104">O método **Cancel** do objeto [**SWbemSink**](swbemsink.md) cancela todas as operações assíncronas pendentes associadas a esse coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="5b524-104">The **Cancel** method of the [**SWbemSink**](swbemsink.md) object cancels all outstanding asynchronous operations that are associated with this object sink.</span></span>

<span data-ttu-id="5b524-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5b524-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b524-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b524-106">Syntax</span></span>


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a><span data-ttu-id="5b524-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b524-107">Parameters</span></span>

<span data-ttu-id="5b524-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5b524-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b524-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b524-109">Return value</span></span>

<span data-ttu-id="5b524-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5b524-110">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5b524-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5b524-111">Error codes</span></span>

<span data-ttu-id="5b524-112">Após a conclusão do método **Cancel** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="5b524-112">After the completion of the **Cancel** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="5b524-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5b524-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5b524-114">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="5b524-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5b524-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5b524-116">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="5b524-116">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-117">**wbemErrTransportFailure** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="5b524-117">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="5b524-118">Ocorreu um erro de rede, impedindo a operação normal.</span><span class="sxs-lookup"><span data-stu-id="5b524-118">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="5b524-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="5b524-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="5b524-120">O nome de usuário e a senha atuais ou especificados não são válidos ou autorizados a estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="5b524-120">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b524-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b524-121">Remarks</span></span>

<span data-ttu-id="5b524-122">Não é possível cancelar apenas uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5b524-122">You cannot cancel only one asynchronous call.</span></span> <span data-ttu-id="5b524-123">Se várias chamadas assíncronas estiverem pendentes que usam esse coletor de objeto, esse método cancelará todas as chamadas assíncronas usando esse coletor de objeto.</span><span class="sxs-lookup"><span data-stu-id="5b524-123">If multiple asynchronous calls are pending that use this object sink, then this method cancels all the asynchronous calls using this object sink.</span></span> <span data-ttu-id="5b524-124">As chamadas assíncronas associadas a outros coletores de objetos continuam inalteradas.</span><span class="sxs-lookup"><span data-stu-id="5b524-124">Asynchronous calls that are associated with other object sinks continue unaffected.</span></span>

<span data-ttu-id="5b524-125">Não é possível atribuir esse coletor a **nada** para cancelar uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5b524-125">You cannot assign this sink to **Nothing** to cancel an asynchronous operation.</span></span> <span data-ttu-id="5b524-126">Você deve chamar o método **Cancel** para tornar o WMI descontinuar a operação e liberar os recursos associados.</span><span class="sxs-lookup"><span data-stu-id="5b524-126">You must call the **Cancel** method to make WMI discontinue the operation and free the associated resources.</span></span> <span data-ttu-id="5b524-127">Isso é muito importante com operações assíncronas demoradas, como consultas ou operações que nunca são concluídas, como [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="5b524-127">This is very important with lengthy asynchronous operations, such as queries, or operations that never complete, such as [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span>

> [!Note]  
> <span data-ttu-id="5b524-128">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="5b524-128">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="5b524-129">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5b524-129">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="5b524-130">Para eliminar os riscos, use semisynchronous ou comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="5b524-130">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="5b524-131">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="5b524-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="5b524-132">O exemplo a seguir mostra como cancelar uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5b524-132">The following example shows you how to cancel an asynchronous call.</span></span>


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a><span data-ttu-id="5b524-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b524-133">Requirements</span></span>



| <span data-ttu-id="5b524-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b524-134">Requirement</span></span> | <span data-ttu-id="5b524-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5b524-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b524-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b524-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5b524-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b524-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b524-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b524-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5b524-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b524-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b524-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b524-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b524-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b524-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b524-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="5b524-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b524-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b524-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5b524-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5b524-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b524-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b524-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5b524-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="5b524-146">CLSID</span></span><br/>                    | <span data-ttu-id="5b524-147">\_SWBEMSINK CLSID</span><span class="sxs-lookup"><span data-stu-id="5b524-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="5b524-148">IID</span><span class="sxs-lookup"><span data-stu-id="5b524-148">IID</span></span><br/>                      | <span data-ttu-id="5b524-149">ISWbemSink de IID \_</span><span class="sxs-lookup"><span data-stu-id="5b524-149">IID\_ISWbemSink</span></span><br/>                                                              |



## <a name="see-also"></a><span data-ttu-id="5b524-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b524-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b524-151">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="5b524-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

