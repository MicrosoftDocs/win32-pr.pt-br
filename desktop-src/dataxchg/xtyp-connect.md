---
title: Transação de XTYP_CONNECT (ddeml. h)
description: Um cliente usa a \_ transação XTYP Connect para estabelecer uma conversa.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- Troca de dados de transação XTYP_CONNECT
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085688"
---
# <a name="xtyp_connect-transaction"></a><span data-ttu-id="8875b-104">Transação do XTYP \_ Connect</span><span class="sxs-lookup"><span data-stu-id="8875b-104">XTYP\_CONNECT transaction</span></span>

<span data-ttu-id="8875b-105">Um cliente usa a transação **XTYP \_ Connect** para estabelecer uma conversa.</span><span class="sxs-lookup"><span data-stu-id="8875b-105">A client uses the **XTYP\_CONNECT** transaction to establish a conversation.</span></span> <span data-ttu-id="8875b-106">Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica um nome de serviço ao qual o servidor dá suporte (e um nome de tópico que não é **nulo**) em uma chamada para a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .</span><span class="sxs-lookup"><span data-stu-id="8875b-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a service name that the server supports (and a topic name that is not **NULL**) in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="8875b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8875b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8875b-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="8875b-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="8875b-109">O tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="8875b-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="8875b-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="8875b-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8875b-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8875b-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8875b-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="8875b-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="8875b-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8875b-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8875b-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="8875b-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="8875b-115">Um identificador para o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="8875b-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="8875b-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="8875b-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="8875b-117">Um identificador para o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="8875b-117">A handle to the service name.</span></span>

</dd> <dt>

<span data-ttu-id="8875b-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="8875b-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="8875b-119">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8875b-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8875b-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="8875b-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="8875b-121">Um ponteiro para uma estrutura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contém informações de contexto para a conversa.</span><span class="sxs-lookup"><span data-stu-id="8875b-121">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="8875b-122">Se o cliente não for um aplicativo DDEML, esse parâmetro será 0.</span><span class="sxs-lookup"><span data-stu-id="8875b-122">If the client is not a DDEML application, this parameter is 0.</span></span>

</dd> <dt>

<span data-ttu-id="8875b-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="8875b-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="8875b-124">Especifica se o cliente é a mesma instância de aplicativo que o servidor.</span><span class="sxs-lookup"><span data-stu-id="8875b-124">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="8875b-125">Se o parâmetro for 1, o cliente será a mesma instância.</span><span class="sxs-lookup"><span data-stu-id="8875b-125">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="8875b-126">Se o parâmetro for 0, o cliente será uma instância diferente.</span><span class="sxs-lookup"><span data-stu-id="8875b-126">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8875b-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8875b-127">Return value</span></span>

<span data-ttu-id="8875b-128">Uma função de retorno de chamada de servidor deve retornar **true** para permitir que o cliente estabeleça uma conversa no nome do serviço especificado e no par do nome do tópico, ou a função deve retornar **false** para negar a conversa.</span><span class="sxs-lookup"><span data-stu-id="8875b-128">A server callback function should return **TRUE** to allow the client to establish a conversation on the specified service name and topic name pair, or the function should return **FALSE** to deny the conversation.</span></span> <span data-ttu-id="8875b-129">Se a função de retorno de chamada retornar **true** e uma conversa for estabelecida com êxito, o sistema passará o identificador de conversa para o servidor emitindo uma transação [**XTYP \_ Connect \_ Confirm**](xtyp-connect-confirm.md) para a função de retorno de chamada do servidor (a menos que o servidor tenha especificado o sinalizador **CBF \_ Skip \_ Connect \_ confirmations** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).</span><span class="sxs-lookup"><span data-stu-id="8875b-129">If the callback function returns **TRUE** and a conversation is successfully established, the system passes the conversation handle to the server by issuing an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's callback function (unless the server specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span>

## <a name="remarks"></a><span data-ttu-id="8875b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="8875b-130">Remarks</span></span>

<span data-ttu-id="8875b-131">Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ Fail \_ Connections** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="8875b-131">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="8875b-132">Um servidor não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.</span><span class="sxs-lookup"><span data-stu-id="8875b-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8875b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8875b-133">Requirements</span></span>



| <span data-ttu-id="8875b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8875b-134">Requirement</span></span> | <span data-ttu-id="8875b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8875b-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8875b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8875b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8875b-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8875b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8875b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8875b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8875b-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8875b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8875b-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8875b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8875b-141"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8875b-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8875b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="8875b-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="8875b-143">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8875b-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8875b-144">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="8875b-144">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="8875b-145">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="8875b-145">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="8875b-146">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="8875b-146">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="8875b-147">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8875b-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8875b-148">troca dinâmica de dados biblioteca de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="8875b-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

