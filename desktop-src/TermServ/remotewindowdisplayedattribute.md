---
title: Enumeração RemoteWindowDisplayedAttribute
description: Usado com o método para especificar informações sobre o evento.
ms.assetid: 22549063-6979-48F2-AEA5-94BFC848C707
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração RemoteWindowDisplayedAttribute
topic_type:
- apiref
api_name:
- RemoteWindowDisplayedAttribute
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137d0ba0b6b692c949ab6c2a0c7b59b0d1fb341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758380"
---
# <a name="remotewindowdisplayedattribute-enumeration"></a><span data-ttu-id="ec0fd-104">Enumeração RemoteWindowDisplayedAttribute</span><span class="sxs-lookup"><span data-stu-id="ec0fd-104">RemoteWindowDisplayedAttribute enumeration</span></span>

<span data-ttu-id="ec0fd-105">Usado com o método para especificar informações sobre o evento.</span><span class="sxs-lookup"><span data-stu-id="ec0fd-105">Used with the method to specify information about the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec0fd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec0fd-106">Syntax</span></span>


```C++
typedef enum  { 
  remoteAppWindowNone          = 0,
  remoteAppWindowDisplayed     = 1,
  remoteAppShellIconDisplayed  = 2
} RemoteWindowDisplayedAttribute;
```



## <a name="constants"></a><span data-ttu-id="ec0fd-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="ec0fd-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ec0fd-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span><span class="sxs-lookup"><span data-stu-id="ec0fd-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="ec0fd-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="ec0fd-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="ec0fd-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span><span class="sxs-lookup"><span data-stu-id="ec0fd-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span></span>
<span data-ttu-id="ec0fd-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ec0fd-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ec0fd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec0fd-112">Requirements</span></span>



| <span data-ttu-id="ec0fd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec0fd-113">Requirement</span></span> | <span data-ttu-id="ec0fd-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ec0fd-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0fd-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec0fd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ec0fd-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ec0fd-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="ec0fd-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec0fd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ec0fd-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec0fd-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="ec0fd-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ec0fd-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec0fd-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec0fd-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec0fd-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec0fd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec0fd-122">**OnRemoteWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="ec0fd-122">**OnRemoteWindowDisplayed**</span></span>](imstscaxevents-onremotewindowdisplayed.md)
</dt> </dl>

 

 





