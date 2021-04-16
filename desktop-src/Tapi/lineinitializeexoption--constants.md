---
description: As \_ constantes LINEINITIALIZEEXOPTION especificam qual mecanismo de notificação de eventos usar ao inicializar uma sessão.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Constantes de LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757961"
---
# <a name="lineinitializeexoption_-constants"></a><span data-ttu-id="26ae2-103">\_Constantes LINEINITIALIZEEXOPTION</span><span class="sxs-lookup"><span data-stu-id="26ae2-103">LINEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="26ae2-104">As **constantes \_ LINEINITIALIZEEXOPTION** especificam qual mecanismo de notificação de eventos usar ao inicializar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="26ae2-104">The **LINEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="26ae2-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="26ae2-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26ae2-106">O aplicativo deseja usar o mecanismo de notificação de evento de controle do hub de chamadas.</span><span class="sxs-lookup"><span data-stu-id="26ae2-106">The application desires to use the call hub tracking event notification mechanism.</span></span> <span data-ttu-id="26ae2-107">Essa constante é exposta somente a aplicativos que negociam uma versão TAPI do 3,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="26ae2-107">This constant is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26ae2-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**</span><span class="sxs-lookup"><span data-stu-id="26ae2-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26ae2-109">O aplicativo deseja usar o mecanismo de notificação de eventos da porta de conclusão.</span><span class="sxs-lookup"><span data-stu-id="26ae2-109">The application desires to use the Completion Port event notification mechanism.</span></span> <span data-ttu-id="26ae2-110">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="26ae2-110">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26ae2-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**</span><span class="sxs-lookup"><span data-stu-id="26ae2-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26ae2-112">O aplicativo deseja usar o mecanismo de notificação de eventos do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="26ae2-112">The application desires to use the Event Handle event notification mechanism.</span></span> <span data-ttu-id="26ae2-113">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="26ae2-113">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="26ae2-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**</span><span class="sxs-lookup"><span data-stu-id="26ae2-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="26ae2-115">O aplicativo deseja usar o mecanismo de notificação de eventos de janela oculta.</span><span class="sxs-lookup"><span data-stu-id="26ae2-115">The application desires to use the Hidden Window event notification mechanism.</span></span> <span data-ttu-id="26ae2-116">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="26ae2-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26ae2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="26ae2-117">Remarks</span></span>

<span data-ttu-id="26ae2-118">Consulte [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) para obter mais detalhes sobre a operação dessas opções.</span><span class="sxs-lookup"><span data-stu-id="26ae2-118">See [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="26ae2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26ae2-119">Requirements</span></span>



| <span data-ttu-id="26ae2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="26ae2-120">Requirement</span></span> | <span data-ttu-id="26ae2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="26ae2-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="26ae2-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="26ae2-122">TAPI version</span></span><br/> | <span data-ttu-id="26ae2-123">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="26ae2-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="26ae2-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26ae2-124">Header</span></span><br/>       | <dl> <span data-ttu-id="26ae2-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ae2-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




