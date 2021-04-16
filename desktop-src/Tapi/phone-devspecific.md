---
description: A TAPI envia a \_ mensagem de telefone DEVSPECIFIC para um aplicativo para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem no telefone. O significado da mensagem e a interpretação dos parâmetros são definidos pela implementação.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Mensagem de PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757615"
---
# <a name="phone_devspecific-message"></a><span data-ttu-id="6b338-104">TELEFONE \_ DEVSPECIFIC mensagem</span><span class="sxs-lookup"><span data-stu-id="6b338-104">PHONE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="6b338-105">A TAPI envia a mensagem de **telefone \_ DEVSPECIFIC** para um aplicativo para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem no telefone.</span><span class="sxs-lookup"><span data-stu-id="6b338-105">TAPI sends the **PHONE\_DEVSPECIFIC** message to an application to notify the application about device-specific events occurring at the phone.</span></span> <span data-ttu-id="6b338-106">O significado da mensagem e a interpretação dos parâmetros são definidos pela implementação.</span><span class="sxs-lookup"><span data-stu-id="6b338-106">The meaning of the message and the interpretation of the parameters is implementation-defined.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6b338-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b338-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b338-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="6b338-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="6b338-109">Um identificador para o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="6b338-109">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="6b338-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6b338-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6b338-111">A instância de retorno de chamada do aplicativo fornecida ao abrir o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="6b338-111">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="6b338-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6b338-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6b338-113">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b338-113">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="6b338-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6b338-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6b338-115">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b338-115">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="6b338-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6b338-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6b338-117">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6b338-117">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b338-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b338-118">Return value</span></span>

<span data-ttu-id="6b338-119">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6b338-119">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b338-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b338-120">Requirements</span></span>



| <span data-ttu-id="6b338-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b338-121">Requirement</span></span> | <span data-ttu-id="6b338-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6b338-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6b338-123">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="6b338-123">TAPI version</span></span><br/> | <span data-ttu-id="6b338-124">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6b338-124">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6b338-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b338-125">Header</span></span><br/>       | <dl> <span data-ttu-id="6b338-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b338-126"><dt>Tapi.h</dt></span></span> </dl> |



 

 




