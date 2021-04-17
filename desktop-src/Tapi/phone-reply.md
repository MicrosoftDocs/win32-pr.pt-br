---
description: A mensagem de resposta do telefone TAPI \_ é enviada a um aplicativo para relatar os resultados da chamada de função que foi concluída de forma assíncrona.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: Mensagem de PHONE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761950"
---
# <a name="phone_reply-message"></a><span data-ttu-id="f1211-103">Mensagem de resposta do telefone \_</span><span class="sxs-lookup"><span data-stu-id="f1211-103">PHONE\_REPLY message</span></span>

<span data-ttu-id="f1211-104">A mensagem **de \_ resposta do telefone** TAPI é enviada a um aplicativo para relatar os resultados da chamada de função que foi concluída de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f1211-104">The TAPI **PHONE\_REPLY** message is sent to an application to report the results of function call that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f1211-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1211-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1211-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="f1211-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="f1211-107">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="f1211-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="f1211-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f1211-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f1211-109">Retorna a instância de retorno de chamada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1211-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="f1211-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f1211-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f1211-111">O identificador de solicitação para o qual esta é a resposta.</span><span class="sxs-lookup"><span data-stu-id="f1211-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="f1211-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f1211-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f1211-113">A indicação de êxito ou erro.</span><span class="sxs-lookup"><span data-stu-id="f1211-113">The success or error indication.</span></span> <span data-ttu-id="f1211-114">O aplicativo deve converter esse parâmetro em um longo.</span><span class="sxs-lookup"><span data-stu-id="f1211-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="f1211-115">Zero indica êxito; um número negativo indica um erro.</span><span class="sxs-lookup"><span data-stu-id="f1211-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="f1211-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f1211-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f1211-117">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="f1211-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1211-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1211-118">Return value</span></span>

<span data-ttu-id="f1211-119">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f1211-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1211-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1211-120">Remarks</span></span>

<span data-ttu-id="f1211-121">As funções que operam de forma assíncrona retornam um valor de identificador de solicitação positivo para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1211-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="f1211-122">Esse identificador de solicitação é retornado com a mensagem de resposta para identificar a solicitação que foi concluída.</span><span class="sxs-lookup"><span data-stu-id="f1211-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="f1211-123">O outro parâmetro para a mensagem de **\_ resposta do telefone** carrega a indicação de êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="f1211-123">The other parameter for the **PHONE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="f1211-124">Os erros possíveis são os mesmos que os definidos pela função correspondente.</span><span class="sxs-lookup"><span data-stu-id="f1211-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="f1211-125">Esta mensagem não pode ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="f1211-125">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1211-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1211-126">Requirements</span></span>



| <span data-ttu-id="f1211-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1211-127">Requirement</span></span> | <span data-ttu-id="f1211-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f1211-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f1211-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="f1211-129">TAPI version</span></span><br/> | <span data-ttu-id="f1211-130">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f1211-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f1211-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1211-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f1211-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1211-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




