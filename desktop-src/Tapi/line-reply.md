---
description: A \_ mensagem de resposta da linha TAPI é enviada para relatar os resultados das chamadas de função que foram concluídas de forma assíncrona.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Mensagem de LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761956"
---
# <a name="line_reply-message"></a><span data-ttu-id="91926-103">Mensagem de resposta de linha \_</span><span class="sxs-lookup"><span data-stu-id="91926-103">LINE\_REPLY message</span></span>

<span data-ttu-id="91926-104">A mensagem **de \_ resposta da linha** TAPI é enviada para relatar os resultados das chamadas de função que foram concluídas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="91926-104">The TAPI **LINE\_REPLY** message is sent to report the results of function calls that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="91926-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91926-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91926-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="91926-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="91926-107">Não usado.</span><span class="sxs-lookup"><span data-stu-id="91926-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="91926-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="91926-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="91926-109">Retorna a instância de retorno de chamada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="91926-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="91926-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="91926-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="91926-111">O identificador de solicitação para o qual esta é a resposta.</span><span class="sxs-lookup"><span data-stu-id="91926-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="91926-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="91926-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="91926-113">A indicação de êxito ou erro.</span><span class="sxs-lookup"><span data-stu-id="91926-113">The success or error indication.</span></span> <span data-ttu-id="91926-114">O aplicativo deve converter esse parâmetro em um longo.</span><span class="sxs-lookup"><span data-stu-id="91926-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="91926-115">Zero indica êxito; um número negativo indica um erro.</span><span class="sxs-lookup"><span data-stu-id="91926-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="91926-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="91926-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="91926-117">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="91926-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91926-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="91926-118">Return value</span></span>

<span data-ttu-id="91926-119">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="91926-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91926-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="91926-120">Remarks</span></span>

<span data-ttu-id="91926-121">As funções que operam de forma assíncrona retornam um valor de identificador de solicitação positivo para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="91926-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="91926-122">Esse identificador de solicitação é retornado com a mensagem de resposta para identificar a solicitação que foi concluída.</span><span class="sxs-lookup"><span data-stu-id="91926-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="91926-123">O outro parâmetro para a mensagem de **\_ resposta de linha** carrega a indicação de êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="91926-123">The other parameter for the **LINE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="91926-124">Os erros possíveis são os mesmos que os definidos pela função correspondente.</span><span class="sxs-lookup"><span data-stu-id="91926-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="91926-125">Esta mensagem não pode ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="91926-125">This message cannot be disabled.</span></span>

<span data-ttu-id="91926-126">Em alguns casos, um aplicativo pode falhar ao receber a mensagem de **\_ resposta de linha** correspondente a uma chamada para uma função assíncrona.</span><span class="sxs-lookup"><span data-stu-id="91926-126">In some cases, an application may fail to receive the **LINE\_REPLY** message corresponding to a call to an asynchronous function.</span></span> <span data-ttu-id="91926-127">Isso ocorrerá se o identificador de chamada correspondente for desalocado antes de a mensagem ser recebida.</span><span class="sxs-lookup"><span data-stu-id="91926-127">This occurs if the corresponding call handle is deallocated before the message has been received.</span></span>

> [!Note]  
> <span data-ttu-id="91926-128">Quando um aplicativo invoca qualquer operação assíncrona que grava dados de volta na memória do aplicativo, o aplicativo deve manter essa memória disponível para gravação até que uma mensagem de **\_ resposta** ou de [**linha \_ GATHERDIGITS**](line-gatherdigits.md) seja recebida.</span><span class="sxs-lookup"><span data-stu-id="91926-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a **LINE\_REPLY** or [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="91926-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91926-129">Requirements</span></span>



| <span data-ttu-id="91926-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="91926-130">Requirement</span></span> | <span data-ttu-id="91926-131">Valor</span><span class="sxs-lookup"><span data-stu-id="91926-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="91926-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="91926-132">TAPI version</span></span><br/> | <span data-ttu-id="91926-133">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="91926-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="91926-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91926-134">Header</span></span><br/>       | <dl> <span data-ttu-id="91926-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="91926-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91926-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="91926-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91926-137">**GATHERDIGITS de linha \_**</span><span class="sxs-lookup"><span data-stu-id="91926-137">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> </dl>

 

 




