---
description: Sinaliza que um comando de navegador de DVD específico foi concluído.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812988"
---
# <a name="ec_dvd_cmd_end"></a><span data-ttu-id="674c2-103">\_fim do \_ cmd de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="674c2-103">EC\_DVD\_CMD\_END</span></span>

<span data-ttu-id="674c2-104">Sinaliza que um comando de [navegador de DVD](dvd-navigator-filter.md) específico foi concluído.</span><span class="sxs-lookup"><span data-stu-id="674c2-104">Signals that a particular [DVD Navigator](dvd-navigator-filter.md) command has completed.</span></span>

## <a name="parameters"></a><span data-ttu-id="674c2-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="674c2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="674c2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="674c2-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="674c2-107">Identificador do comando.</span><span class="sxs-lookup"><span data-stu-id="674c2-107">Command identifier.</span></span> <span data-ttu-id="674c2-108">Passe este parâmetro para o método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) para recuperar um ponteiro de interface [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .</span><span class="sxs-lookup"><span data-stu-id="674c2-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="674c2-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="674c2-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="674c2-110">Valor **HRESULT** que indica o status do comando.</span><span class="sxs-lookup"><span data-stu-id="674c2-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="674c2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="674c2-111">Remarks</span></span>

<span data-ttu-id="674c2-112">Esse evento só será disparado se o aplicativo definir o sinalizador de sinalizador de comando de DVD \_ \_ \_ SendEvents em um método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) que usa um sinalizador de [**\_ \_ sinalizadores de DVD cmd**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .</span><span class="sxs-lookup"><span data-stu-id="674c2-112">This event is only fired if your application sets the DVD\_CMD\_FLAG\_SendEvents flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="674c2-113">Esse evento é gerado no domínio do título.</span><span class="sxs-lookup"><span data-stu-id="674c2-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="674c2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="674c2-114">Requirements</span></span>



| <span data-ttu-id="674c2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="674c2-115">Requirement</span></span> | <span data-ttu-id="674c2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="674c2-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="674c2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="674c2-117">Header</span></span><br/> | <dl> <span data-ttu-id="674c2-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="674c2-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="674c2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="674c2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="674c2-120">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="674c2-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="674c2-121">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="674c2-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="674c2-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="674c2-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="674c2-123">Sincronizando comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="674c2-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




