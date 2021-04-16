---
description: A mensagem de APPNEWCALLHUB de linha TAPI \_ é enviada para informar um aplicativo quando um novo hub de chamadas tiver sido criado.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Mensagem de LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759464"
---
# <a name="line_appnewcallhub-message"></a><span data-ttu-id="a6376-103">Mensagem de APPNEWCALLHUB de linha \_</span><span class="sxs-lookup"><span data-stu-id="a6376-103">LINE\_APPNEWCALLHUB message</span></span>

<span data-ttu-id="a6376-104">A mensagem **de \_ APPNEWCALLHUB de linha** TAPI é enviada para informar um aplicativo quando um novo hub de chamadas tiver sido criado.</span><span class="sxs-lookup"><span data-stu-id="a6376-104">The TAPI **LINE\_APPNEWCALLHUB** message is sent to inform an application when a new call hub has been created.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="a6376-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6376-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6376-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="a6376-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a6376-107">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="a6376-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="a6376-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="a6376-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="a6376-109">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="a6376-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="a6376-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="a6376-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="a6376-111">O nível de rastreamento no novo hub, conforme definido por uma das [**\_ constantes LINECALLHUBTRACKING**](linecallhubtracking--constants.md).</span><span class="sxs-lookup"><span data-stu-id="a6376-111">The tracking level on the new hub, as defined by one of the [**LINECALLHUBTRACKING\_ Constants**](linecallhubtracking--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6376-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6376-112">Return value</span></span>

<span data-ttu-id="a6376-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a6376-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6376-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6376-114">Remarks</span></span>

<span data-ttu-id="a6376-115">Essa mensagem é originada com TAPI em vez de com um provedor de serviços, portanto, não há nenhuma mensagem TSPI correspondente.</span><span class="sxs-lookup"><span data-stu-id="a6376-115">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6376-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6376-116">Requirements</span></span>



| <span data-ttu-id="a6376-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6376-117">Requirement</span></span> | <span data-ttu-id="a6376-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a6376-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a6376-119">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="a6376-119">TAPI version</span></span><br/> | <span data-ttu-id="a6376-120">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="a6376-120">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="a6376-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6376-121">Header</span></span><br/>       | <dl> <span data-ttu-id="a6376-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6376-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




