---
description: O grafo está abrindo um arquivo ou terminou de abrir um arquivo.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758469"
---
# <a name="ec_opening_file"></a><span data-ttu-id="4d042-103">\_arquivo de abertura do EC \_</span><span class="sxs-lookup"><span data-stu-id="4d042-103">EC\_OPENING\_FILE</span></span>

<span data-ttu-id="4d042-104">O grafo está abrindo um arquivo ou terminou de abrir um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4d042-104">The graph is opening a file, or has finished opening a file.</span></span>

## <a name="parameters"></a><span data-ttu-id="4d042-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d042-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d042-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="4d042-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="4d042-107">**True** se o grafo estiver começando a abrir um arquivo ou **false** se o grafo não estiver mais abrindo o arquivo.</span><span class="sxs-lookup"><span data-stu-id="4d042-107">**TRUE** if the graph is starting to open a file, or **FALSE** if the graph is no longer opening the file.</span></span>

</dd> <dt>

<span data-ttu-id="4d042-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="4d042-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="4d042-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="4d042-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="4d042-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="4d042-110">Default Action</span></span>

<span data-ttu-id="4d042-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4d042-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d042-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d042-112">Remarks</span></span>

<span data-ttu-id="4d042-113">Um filtro pode enviar esse evento se ele gastar um tempo significativo abrindo um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4d042-113">A filter can send this event if it spends significant time opening a file.</span></span> <span data-ttu-id="4d042-114">(Por exemplo, o arquivo pode estar localizado em uma rede). O aplicativo pode usar esse evento para ajustar sua interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4d042-114">(For example, the file might be located on a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d042-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d042-115">Requirements</span></span>



| <span data-ttu-id="4d042-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d042-116">Requirement</span></span> | <span data-ttu-id="4d042-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4d042-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d042-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d042-118">Header</span></span><br/> | <dl> <span data-ttu-id="4d042-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d042-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d042-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d042-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d042-121">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="4d042-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="4d042-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="4d042-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




