---
description: As \_ constantes de sinalizador de bit LINEDEVSTATUSFLAGS descrevem uma coleção de itens de status de dispositivo de linha booliana.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Constantes de LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764758"
---
# <a name="linedevstatusflags_-constants"></a><span data-ttu-id="3dc77-103">\_Constantes LINEDEVSTATUSFLAGS</span><span class="sxs-lookup"><span data-stu-id="3dc77-103">LINEDEVSTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="3dc77-104">As constantes de sinalizador de bit **LINEDEVSTATUSFLAGS \_** descrevem uma coleção de itens de status de dispositivo de linha booliana.</span><span class="sxs-lookup"><span data-stu-id="3dc77-104">The **LINEDEVSTATUSFLAGS\_** bit-flag constants describe a collection of Boolean line device status items.</span></span>

<dl> <dt>

<span data-ttu-id="3dc77-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="3dc77-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3dc77-106">Especifica se a linha está conectada à TAPI.</span><span class="sxs-lookup"><span data-stu-id="3dc77-106">Specifies whether the line is connected to TAPI.</span></span> <span data-ttu-id="3dc77-107">Se for **true**, a linha será conectada e a TAPI será capaz de operar no dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3dc77-107">If **TRUE**, the line is connected and TAPI is able to operate on the line device.</span></span> <span data-ttu-id="3dc77-108">Se for **false**, a linha será desconectada e o aplicativo não poderá controlar o dispositivo de linha por meio da TAPI.</span><span class="sxs-lookup"><span data-stu-id="3dc77-108">If **FALSE**, the line is disconnected and the application is unable to control the line device through TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dc77-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INserviço**</span><span class="sxs-lookup"><span data-stu-id="3dc77-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3dc77-110">Indica se a linha está em serviço.</span><span class="sxs-lookup"><span data-stu-id="3dc77-110">Indicates whether the line is in service.</span></span> <span data-ttu-id="3dc77-111">Se for **true**, a linha estará em serviço; Se for **false**, a linha estará fora do serviço.</span><span class="sxs-lookup"><span data-stu-id="3dc77-111">If **TRUE**, the line is in service; if **FALSE**, the line is out of service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dc77-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="3dc77-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3dc77-113">Indica se a linha está bloqueada ou desbloqueada.</span><span class="sxs-lookup"><span data-stu-id="3dc77-113">Indicates whether the line is locked or unlocked.</span></span> <span data-ttu-id="3dc77-114">Esse bit é usado com mais frequência com dispositivos de linha associados a telefones celulares.</span><span class="sxs-lookup"><span data-stu-id="3dc77-114">This bit is most often used with line devices associated with cellular phones.</span></span> <span data-ttu-id="3dc77-115">Muitos telefones celulares têm um mecanismo de segurança que exige a entrada de uma senha para permitir que o telefone faça chamadas.</span><span class="sxs-lookup"><span data-stu-id="3dc77-115">Many cellular phones have a security mechanism that requires the entry of a password to enable the phone to place calls.</span></span> <span data-ttu-id="3dc77-116">Esse bit pode ser usado para indicar aos aplicativos que o telefone está bloqueado e não pode fazer chamadas até que a senha seja inserida na interface do usuário do telefone para que o aplicativo possa apresentar um alerta apropriado ao usuário.</span><span class="sxs-lookup"><span data-stu-id="3dc77-116">This bit can be used to indicate to applications that the phone is locked and cannot place calls until the password is entered on the user interface of the phone so that the application can present an appropriate alert to the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dc77-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**</span><span class="sxs-lookup"><span data-stu-id="3dc77-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS\_MSGWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="3dc77-118">Indica se a linha tem uma mensagem aguardando.</span><span class="sxs-lookup"><span data-stu-id="3dc77-118">Indicates whether the line has a message waiting.</span></span> <span data-ttu-id="3dc77-119">Se for **true**, uma mensagem estará aguardando; Se for **false**, nenhuma mensagem estará aguardando.</span><span class="sxs-lookup"><span data-stu-id="3dc77-119">If **TRUE**, a message is waiting; if **FALSE**, no message is waiting.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3dc77-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dc77-120">Remarks</span></span>

<span data-ttu-id="3dc77-121">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="3dc77-121">No extensibility.</span></span> <span data-ttu-id="3dc77-122">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="3dc77-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="3dc77-123">\_As constantes LINEDEVSTATUSFLAGS são usadas dentro do membro **dwDevStatusFlags** da estrutura de dados [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="3dc77-123">LINEDEVSTATUSFLAGS\_ constants are used within the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc77-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dc77-124">Requirements</span></span>



| <span data-ttu-id="3dc77-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dc77-125">Requirement</span></span> | <span data-ttu-id="3dc77-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3dc77-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3dc77-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3dc77-127">TAPI version</span></span><br/> | <span data-ttu-id="3dc77-128">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3dc77-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="3dc77-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3dc77-129">Header</span></span><br/>       | <dl> <span data-ttu-id="3dc77-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dc77-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




