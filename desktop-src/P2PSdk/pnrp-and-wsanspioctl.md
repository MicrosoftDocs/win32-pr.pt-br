---
description: O PNRP usa a função WSANSPIoctl para receber notificações sobre alterações no seguinte.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP e WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753944"
---
# <a name="pnrp-and-wsanspioctl"></a><span data-ttu-id="ad688-103">PNRP e WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="ad688-103">PNRP and WSANSPIoctl</span></span>

<span data-ttu-id="ad688-104">O PNRP usa a função [**WSANSPIoctl**](winsock-nsp-reference-links.md) para receber notificações sobre as alterações feitas no seguinte:</span><span class="sxs-lookup"><span data-stu-id="ad688-104">PNRP uses the [**WSANSPIoctl**](winsock-nsp-reference-links.md) function to receive notifications about changes to the following:</span></span>

-   <span data-ttu-id="ad688-105">Uma lista de nuvem de rede</span><span class="sxs-lookup"><span data-stu-id="ad688-105">A network cloud list</span></span>
-   <span data-ttu-id="ad688-106">Disponibilidade de resultados de uma solicitação de resolução de nomes</span><span class="sxs-lookup"><span data-stu-id="ad688-106">Availability of results of a name resolution request</span></span>

<span data-ttu-id="ad688-107">A primeira chamada para [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) define o tipo de informações sobre as quais um cliente é notificado.</span><span class="sxs-lookup"><span data-stu-id="ad688-107">The first call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) defines the type of information that a client is notified about.</span></span> <span data-ttu-id="ad688-108">Um cliente pode ser notificado com uma mensagem do Windows, uma rotina de conclusão, um identificador para um objeto WSAEVENT ou uma porta.</span><span class="sxs-lookup"><span data-stu-id="ad688-108">A client can be notified with a Windows message, a completion routine, a handle to a WSAEVENT object, or a port.</span></span> <span data-ttu-id="ad688-109">Para obter mais informações sobre as opções e definir o parâmetro *lpCompletion* , consulte **WSANSPIoctl**.</span><span class="sxs-lookup"><span data-stu-id="ad688-109">For more information about options and setting the *lpCompletion* parameter, see **WSANSPIoctl**.</span></span>

<span data-ttu-id="ad688-110">Para continuar recebendo notificações após uma chamada para [**WSALookupServiceNext**](winsock-nsp-reference-links.md), um aplicativo deve chamar **WSANSPIoctl** novamente.</span><span class="sxs-lookup"><span data-stu-id="ad688-110">To continue receiving notifications after a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md), an application must call **WSANSPIoctl** again.</span></span>

<span data-ttu-id="ad688-111">A função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) é bloqueada mesmo se **WSANSPIoctl** for chamado.</span><span class="sxs-lookup"><span data-stu-id="ad688-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="ad688-112">Antes de chamar **WSALookupServiceNext**, um aplicativo deve aguardar até receber uma notificação — se o bloqueio for um problema.</span><span class="sxs-lookup"><span data-stu-id="ad688-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

<span data-ttu-id="ad688-113">Ao chamar essa função, os parâmetros devem ter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ad688-113">When calling this function, the parameters must have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ad688-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span><span class="sxs-lookup"><span data-stu-id="ad688-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span></span>
</dt> <dd>

<span data-ttu-id="ad688-115">Especifica o identificador que [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) retorna.</span><span class="sxs-lookup"><span data-stu-id="ad688-115">Specifies the handle that [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) returns.</span></span>

</dd> <dt>

<span data-ttu-id="ad688-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span><span class="sxs-lookup"><span data-stu-id="ad688-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span></span>
</dt> <dd>

<span data-ttu-id="ad688-117">Deve ser **sio \_ NSP \_ notificar \_ alteração**.</span><span class="sxs-lookup"><span data-stu-id="ad688-117">Must be **SIO\_NSP\_NOTIFY\_CHANGE**.</span></span>

</dd> <dt>

<span data-ttu-id="ad688-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span><span class="sxs-lookup"><span data-stu-id="ad688-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="ad688-119">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ad688-119">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ad688-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span><span class="sxs-lookup"><span data-stu-id="ad688-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="ad688-121">Deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="ad688-121">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="ad688-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="ad688-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="ad688-123">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ad688-123">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ad688-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="ad688-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="ad688-125">Deve ser zero (0).</span><span class="sxs-lookup"><span data-stu-id="ad688-125">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="ad688-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="ad688-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span></span>
</dt> <dd>

<span data-ttu-id="ad688-127">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ad688-127">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ad688-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span><span class="sxs-lookup"><span data-stu-id="ad688-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span></span>
</dt> <dd>

<span data-ttu-id="ad688-129">Especifica o **NULL** ou um ponteiro para uma estrutura [**WSACOMPLETION**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="ad688-129">Specifies either **NULL** or a pointer to a [**WSACOMPLETION**](winsock-nsp-reference-links.md) structure.</span></span>

</dd> </dl>

<span data-ttu-id="ad688-130">Depois que uma notificação for recebida, chame [**WSALookupServiceNext**](winsock-nsp-reference-links.md) uma vez para obter os resultados.</span><span class="sxs-lookup"><span data-stu-id="ad688-130">After a notification is received, call [**WSALookupServiceNext**](winsock-nsp-reference-links.md) one time to obtain the results.</span></span>

<span data-ttu-id="ad688-131">Para encerrar uma pesquisa, chame [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span><span class="sxs-lookup"><span data-stu-id="ad688-131">To end a search, call [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span></span>

## <a name="resolution-notifications"></a><span data-ttu-id="ad688-132">Notificações de resolução</span><span class="sxs-lookup"><span data-stu-id="ad688-132">Resolution Notifications</span></span>

<span data-ttu-id="ad688-133">Um cliente pode ser notificado sempre que uma entrada de resolução de nome for adicionada.</span><span class="sxs-lookup"><span data-stu-id="ad688-133">A client can be notified any time that a name resolution entry is added.</span></span> <span data-ttu-id="ad688-134">Em seguida, o cliente chama [**WSALookupServiceNext**](winsock-nsp-reference-links.md) para obter os dados de resolução.</span><span class="sxs-lookup"><span data-stu-id="ad688-134">The client then calls [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to obtain the resolution data.</span></span>

<span data-ttu-id="ad688-135">Se o cliente não usar essa técnica, uma chamada para [**WSALookupServiceNext**](winsock-nsp-reference-links.md) poderá ser bloqueada até que o tempo limite especificado ocorra.</span><span class="sxs-lookup"><span data-stu-id="ad688-135">If the client does not use this technique, a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) can be blocked until the specified timeout occurs.</span></span>

## <a name="cloud-list-notifications"></a><span data-ttu-id="ad688-136">Notificações da lista de nuvem</span><span class="sxs-lookup"><span data-stu-id="ad688-136">Cloud List Notifications</span></span>

<span data-ttu-id="ad688-137">Um cliente pode ser notificado sempre que houver uma alteração em um conjunto de nuvens.</span><span class="sxs-lookup"><span data-stu-id="ad688-137">A client can be notified any time there is a change to a set of clouds.</span></span>

<span data-ttu-id="ad688-138">A função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) retorna **WSA \_ E \_ não \_ mais** como um delimitador de conjunto.</span><span class="sxs-lookup"><span data-stu-id="ad688-138">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns **WSA\_E\_NO\_MORE** as a set delimiter.</span></span> <span data-ttu-id="ad688-139">O aplicativo cliente deve enumerar nuvens existentes até que essa mensagem seja retornada e, em seguida, usar um esquema de notificação para recuperar alterações subsequentes conforme elas ocorrem.</span><span class="sxs-lookup"><span data-stu-id="ad688-139">The client application must enumerate existing clouds until this message is returned, and then use a notification scheme to retrieve subsequent changes as they occur.</span></span> <span data-ttu-id="ad688-140">Um aplicativo cliente também pode chamar **WSALookupServiceNext**, mas a chamada é bloqueada até que ocorra uma alteração.</span><span class="sxs-lookup"><span data-stu-id="ad688-140">A client application can also call **WSALookupServiceNext**, but the call is blocked until a change occurs.</span></span>

<span data-ttu-id="ad688-141">A função [**WSALookupServiceNext**](winsock-nsp-reference-links.md) retorna uma nuvem em uma estrutura **WSAQUERYSET** .</span><span class="sxs-lookup"><span data-stu-id="ad688-141">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns a cloud in a **WSAQUERYSET** structure.</span></span> <span data-ttu-id="ad688-142">Um dos sinalizadores a seguir é retornado no membro **dwOutputFlags** .</span><span class="sxs-lookup"><span data-stu-id="ad688-142">One of the following flags is returned in the **dwOutputFlags** member.</span></span>



| <span data-ttu-id="ad688-143">Valor</span><span class="sxs-lookup"><span data-stu-id="ad688-143">Value</span></span>               | <span data-ttu-id="ad688-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad688-144">Description</span></span>                                             |
|---------------------|---------------------------------------------------------|
| <span data-ttu-id="ad688-145">o resultado \_ é \_ adicionado</span><span class="sxs-lookup"><span data-stu-id="ad688-145">RESULT\_IS\_ADDED</span></span>   | <span data-ttu-id="ad688-146">A nuvem retornada é adicionada.</span><span class="sxs-lookup"><span data-stu-id="ad688-146">The cloud that is returned is added.</span></span>                    |
| <span data-ttu-id="ad688-147">o resultado \_ é \_ alterado</span><span class="sxs-lookup"><span data-stu-id="ad688-147">RESULT\_IS\_CHANGED</span></span> | <span data-ttu-id="ad688-148">A nuvem retornada é alterada.</span><span class="sxs-lookup"><span data-stu-id="ad688-148">The cloud that is returned is changed.</span></span>                  |
| <span data-ttu-id="ad688-149">o resultado \_ é \_ excluído</span><span class="sxs-lookup"><span data-stu-id="ad688-149">RESULT\_IS\_DELETED</span></span> | <span data-ttu-id="ad688-150">A nuvem retornada é excluída e não é válida.</span><span class="sxs-lookup"><span data-stu-id="ad688-150">The cloud that is returned is deleted and is not valid.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ad688-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad688-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad688-152">PNRP e WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="ad688-152">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="ad688-153">PNRP e WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="ad688-153">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="ad688-154">PNRP e WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="ad688-154">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="ad688-155">Códigos de erro NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="ad688-155">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="ad688-156">**WSANSPIoctl**</span><span class="sxs-lookup"><span data-stu-id="ad688-156">**WSANSPIoctl**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="ad688-157">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="ad688-157">**WSALookupServiceBegin**</span></span>
</dt> <dt>

<span data-ttu-id="ad688-158">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="ad688-158">**WSALookupServiceEnd**</span></span>
</dt> <dt>

<span data-ttu-id="ad688-159">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="ad688-159">**WSAQUERYSET**</span></span>
</dt> </dl>

 

 



