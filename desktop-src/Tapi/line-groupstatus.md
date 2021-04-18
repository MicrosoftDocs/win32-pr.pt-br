---
description: A mensagem de linha \_ GROUPSTATUS é enviada quando o status de um grupo de AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Mensagem de LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757619"
---
# <a name="line_groupstatus-message"></a><span data-ttu-id="07553-104">Mensagem de GROUPSTATUS de linha \_</span><span class="sxs-lookup"><span data-stu-id="07553-104">LINE\_GROUPSTATUS message</span></span>

<span data-ttu-id="07553-105">A mensagem de **linha \_ GROUPSTATUS** é enviada quando o status de um grupo de AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta.</span><span class="sxs-lookup"><span data-stu-id="07553-105">The **LINE\_GROUPSTATUS** message is sent when the status of an ACD group changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="07553-106">Essa mensagem é gerada usando a função [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="07553-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="07553-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07553-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07553-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="07553-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="07553-109">O identificador do aplicativo para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="07553-109">The application's handle to the line device.</span></span> <span data-ttu-id="07553-110">Isso está relacionado ao manipulador do agente.</span><span class="sxs-lookup"><span data-stu-id="07553-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="07553-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="07553-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="07553-112">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="07553-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="07553-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="07553-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="07553-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="07553-114">Reserved.</span></span> <span data-ttu-id="07553-115">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="07553-115">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="07553-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="07553-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="07553-117">Especifica o status do grupo que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="07553-117">Specifies the group status that has changed.</span></span> <span data-ttu-id="07553-118">O aplicativo pode invocar [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) para determinar as alterações nos grupos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="07553-118">The application can invoke [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) to determine the changes in available groups.</span></span> <span data-ttu-id="07553-119">O parâmetro *dwParam2* é uma ou mais das [**\_ constantes LINEGROUPSTATUS**](linegroupstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="07553-119">The *dwParam2* parameter is one or more of the [**LINEGROUPSTATUS\_ constants**](linegroupstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="07553-120">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="07553-120">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="07553-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="07553-121">Reserved.</span></span> <span data-ttu-id="07553-122">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="07553-122">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07553-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07553-123">Requirements</span></span>



| <span data-ttu-id="07553-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="07553-124">Requirement</span></span> | <span data-ttu-id="07553-125">Valor</span><span class="sxs-lookup"><span data-stu-id="07553-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="07553-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="07553-126">TAPI version</span></span><br/> | <span data-ttu-id="07553-127">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="07553-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="07553-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07553-128">Header</span></span><br/>       | <dl> <span data-ttu-id="07553-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="07553-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07553-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="07553-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07553-131">**lineGetGroupList**</span><span class="sxs-lookup"><span data-stu-id="07553-131">**lineGetGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




