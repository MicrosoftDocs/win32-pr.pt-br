---
description: Sinaliza que um comando de DVD Navigator foi iniciado.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0fb723b220bf8aa12baa7133c9985225d6051921
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752479"
---
# <a name="ec_dvd_cmd_start"></a><span data-ttu-id="d63eb-103">\_início do \_ cmd de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="d63eb-103">EC\_DVD\_CMD\_START</span></span>

<span data-ttu-id="d63eb-104">Sinaliza que um comando de [DVD Navigator](dvd-navigator-filter.md) foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="d63eb-104">Signals that a [DVD Navigator](dvd-navigator-filter.md) command has begun.</span></span>

## <a name="parameters"></a><span data-ttu-id="d63eb-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d63eb-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d63eb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="d63eb-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="d63eb-107">Identificador do comando.</span><span class="sxs-lookup"><span data-stu-id="d63eb-107">Command identifier.</span></span> <span data-ttu-id="d63eb-108">Passe este parâmetro para o método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) para recuperar um ponteiro de interface [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .</span><span class="sxs-lookup"><span data-stu-id="d63eb-108">Pass this parameter to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method to retrieve an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) interface pointer.</span></span>

</dd> <dt>

<span data-ttu-id="d63eb-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="d63eb-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="d63eb-110">Valor **HRESULT** que indica o status do comando.</span><span class="sxs-lookup"><span data-stu-id="d63eb-110">**HRESULT** value indicating the status of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d63eb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d63eb-111">Remarks</span></span>

<span data-ttu-id="d63eb-112">Esse evento só será disparado se o aplicativo definir o sinalizador de **sinalizador de comando de DVD \_ \_ \_ SendEvents** em um método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) que usa um sinalizador de [**sinalizadores de DVD \_ cmd \_**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .</span><span class="sxs-lookup"><span data-stu-id="d63eb-112">This event is only fired if your application sets the **DVD\_CMD\_FLAG\_SendEvents** flag in an [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method that takes a [**DVD\_CMD\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) flag.</span></span>

<span data-ttu-id="d63eb-113">Esse evento é gerado no domínio do título.</span><span class="sxs-lookup"><span data-stu-id="d63eb-113">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63eb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d63eb-114">Requirements</span></span>



| <span data-ttu-id="d63eb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d63eb-115">Requirement</span></span> | <span data-ttu-id="d63eb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d63eb-116">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d63eb-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d63eb-117">Header</span></span><br/> | <dl> <span data-ttu-id="d63eb-118"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d63eb-118"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d63eb-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d63eb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63eb-120">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="d63eb-120">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="d63eb-121">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="d63eb-121">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="d63eb-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="d63eb-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d63eb-123">Sincronizando comandos de DVD</span><span class="sxs-lookup"><span data-stu-id="d63eb-123">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




