---
title: Enumeração RemoteSessionActionType
description: Usado para especificar o tipo de ação remota.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração RemoteSessionActionType
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761327"
---
# <a name="remotesessionactiontype-enumeration"></a><span data-ttu-id="29e85-104">Enumeração RemoteSessionActionType</span><span class="sxs-lookup"><span data-stu-id="29e85-104">RemoteSessionActionType enumeration</span></span>

<span data-ttu-id="29e85-105">Usado para especificar o tipo de ação remota.</span><span class="sxs-lookup"><span data-stu-id="29e85-105">Used to specify the type of remote action.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e85-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="29e85-106">Syntax</span></span>


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a><span data-ttu-id="29e85-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="29e85-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="29e85-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span><span class="sxs-lookup"><span data-stu-id="29e85-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span></span>
</dt> <dd>

<span data-ttu-id="29e85-109">Exibe os botões na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="29e85-109">Displays the charms in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="29e85-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span><span class="sxs-lookup"><span data-stu-id="29e85-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span></span>
</dt> <dd>

<span data-ttu-id="29e85-111">Exibe a barra de aplicativos na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="29e85-111">Displays the app bar in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="29e85-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span><span class="sxs-lookup"><span data-stu-id="29e85-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span></span>
</dt> <dd>

<span data-ttu-id="29e85-113">Encaixa o aplicativo na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="29e85-113">Docks the application in the remote session.</span></span> <span data-ttu-id="29e85-114">Esta opção foi preterida e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="29e85-114">This option has been deprecated and should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="29e85-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span><span class="sxs-lookup"><span data-stu-id="29e85-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span></span>
</dt> <dd>

<span data-ttu-id="29e85-116">Faz com que a tela inicial seja exibida na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="29e85-116">Causes the start screen to be displayed in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="29e85-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span><span class="sxs-lookup"><span data-stu-id="29e85-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span></span>
</dt> <dd>

<span data-ttu-id="29e85-118">Faz com que a janela de comutador do aplicativo seja exibida na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="29e85-118">Causes the application switch window to be displayed in the remote session.</span></span> <span data-ttu-id="29e85-119">Isso é o mesmo que o usuário pressionando Alt + Tab.</span><span class="sxs-lookup"><span data-stu-id="29e85-119">This is the same as the user pressing Alt+Tab.</span></span>

</dd> <dt>

<span data-ttu-id="29e85-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span><span class="sxs-lookup"><span data-stu-id="29e85-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span></span>
</dt> <dd>

<span data-ttu-id="29e85-121">Faz com que a central de ações seja exibida na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="29e85-121">Causes the Action Center to be displayed in the remote session.</span></span> <span data-ttu-id="29e85-122">Isso é o mesmo que o usuário pressionando Win + A.</span><span class="sxs-lookup"><span data-stu-id="29e85-122">This is the same as the user pressing Win+A.</span></span>

<span data-ttu-id="29e85-123">**Windows server 2012 R2, Windows 8.1, Windows server 2012 e Windows 8:** Não há suporte para esse valor antes do Windows Server 2016 e do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="29e85-123">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:** This value is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29e85-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29e85-124">Requirements</span></span>



| <span data-ttu-id="29e85-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="29e85-125">Requirement</span></span> | <span data-ttu-id="29e85-126">Valor</span><span class="sxs-lookup"><span data-stu-id="29e85-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29e85-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29e85-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29e85-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="29e85-128">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="29e85-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29e85-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29e85-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="29e85-130">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="29e85-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="29e85-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="29e85-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29e85-132"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29e85-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="29e85-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e85-134">**IMsRdpClient8::SendRemoteAction**</span><span class="sxs-lookup"><span data-stu-id="29e85-134">**IMsRdpClient8::SendRemoteAction**</span></span>](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





