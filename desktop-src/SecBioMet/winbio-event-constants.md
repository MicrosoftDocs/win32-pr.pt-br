---
title: Constantes de WINBIO_EVENT (WinBio \_ Types. h)
description: Especifique os tipos de notificações de eventos do provedor de serviços a serem monitorados.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499273"
---
# <a name="winbio_event-constants"></a><span data-ttu-id="01300-103">\_Constantes de evento WINBIO</span><span class="sxs-lookup"><span data-stu-id="01300-103">WINBIO\_EVENT Constants</span></span>

<span data-ttu-id="01300-104">As constantes a seguir podem ser usadas na função [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para especificar os tipos de notificações de eventos do provedor de serviços a serem monitorados.</span><span class="sxs-lookup"><span data-stu-id="01300-104">The following constants can be used in the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to specify the types of service provider event notifications to monitor.</span></span>



| <span data-ttu-id="01300-105">Constante</span><span class="sxs-lookup"><span data-stu-id="01300-105">Constant</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="01300-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="01300-106">Description</span></span>                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <span data-ttu-id="01300-107"><dt>**\_evento WINBIO \_ FP não \_ reclamado**</dt></span><span class="sxs-lookup"><span data-stu-id="01300-107"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED**</dt></span></span> </dl>                             | <span data-ttu-id="01300-108">O sensor detectou um dedo de dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco.</span><span class="sxs-lookup"><span data-stu-id="01300-108">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="01300-109">O Windows Biometric Framework chama sua função de retorno de chamada para indicar que um dedo dedo ocorreu, mas não tenta identificar a impressão digital.</span><span class="sxs-lookup"><span data-stu-id="01300-109">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.</span></span><br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <span data-ttu-id="01300-110"><dt>**\_identificação não \_ reivindicada de FP do evento \_ WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="01300-110"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY**</dt></span></span> </dl> | <span data-ttu-id="01300-111">O sensor detectou um dedo de dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco.</span><span class="sxs-lookup"><span data-stu-id="01300-111">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="01300-112">O Windows Biometric Framework tenta identificar a impressão digital e passa o resultado desse processo para sua função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="01300-112">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="01300-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01300-113">Requirements</span></span>



| <span data-ttu-id="01300-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="01300-114">Requirement</span></span> | <span data-ttu-id="01300-115">Valor</span><span class="sxs-lookup"><span data-stu-id="01300-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01300-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01300-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01300-117">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01300-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="01300-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01300-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01300-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="01300-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="01300-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01300-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01300-121"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01300-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01300-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="01300-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01300-123">Constantes de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="01300-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





