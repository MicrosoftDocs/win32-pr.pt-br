---
description: A propriedade PROMPTROLLBACKCOST especifica a ação que o instalador executará se os recursos de reversão da instalação estiverem habilitados e não houver espaço em disco suficiente para concluir a instalação. Os valores possíveis de PROMPTROLLBACKCOST são os seguintes. ValueActionPDisplay uma caixa de diálogo perguntando se deseja continuar sem uma reversão. DDisable reversão e continue sem perguntar ao usuário. FFail com a solicitação de erro de espaço em disco insuficiente.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Propriedade PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751425"
---
# <a name="promptrollbackcost-property"></a><span data-ttu-id="32ca1-103">Propriedade PROMPTROLLBACKCOST</span><span class="sxs-lookup"><span data-stu-id="32ca1-103">PROMPTROLLBACKCOST property</span></span>

<span data-ttu-id="32ca1-104">A propriedade **PROMPTROLLBACKCOST** especifica a ação que o instalador executará se os recursos de [reversão da instalação](rollback-installation.md) estiverem habilitados e não houver espaço em disco suficiente para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="32ca1-104">The **PROMPTROLLBACKCOST** property specifies the action the installer takes if [rollback installation](rollback-installation.md) capabilities are enabled and there is insufficient disk space to complete the installation.</span></span>

<span data-ttu-id="32ca1-105">Os valores possíveis de **PROMPTROLLBACKCOST** são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="32ca1-105">The possible values of **PROMPTROLLBACKCOST** are as follows.</span></span>



| <span data-ttu-id="32ca1-106">Valor</span><span class="sxs-lookup"><span data-stu-id="32ca1-106">Value</span></span> | <span data-ttu-id="32ca1-107">Ação</span><span class="sxs-lookup"><span data-stu-id="32ca1-107">Action</span></span>                                                              |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="32ca1-108">P</span><span class="sxs-lookup"><span data-stu-id="32ca1-108">P</span></span>     | <span data-ttu-id="32ca1-109">Exibir uma caixa de diálogo perguntando se deseja continuar sem uma reversão.</span><span class="sxs-lookup"><span data-stu-id="32ca1-109">Display a dialog box asking whether to continue without a rollback.</span></span> |
| <span data-ttu-id="32ca1-110">D</span><span class="sxs-lookup"><span data-stu-id="32ca1-110">D</span></span>     | <span data-ttu-id="32ca1-111">Desabilite a reversão e continue sem perguntar ao usuário.</span><span class="sxs-lookup"><span data-stu-id="32ca1-111">Disable rollback and continue without asking user.</span></span>                  |
| <span data-ttu-id="32ca1-112">F</span><span class="sxs-lookup"><span data-stu-id="32ca1-112">F</span></span>     | <span data-ttu-id="32ca1-113">Falha com a solicitação de erro de espaço em disco insuficiente.</span><span class="sxs-lookup"><span data-stu-id="32ca1-113">Fail with the out-of-disk-space error prompt.</span></span>                       |



 

## <a name="remarks"></a><span data-ttu-id="32ca1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="32ca1-114">Remarks</span></span>

<span data-ttu-id="32ca1-115">Quando a interface do usuário é executada no nível básico ou sem interface do usuário, o instalador manipula toda a lógica de espaço em disco automaticamente.</span><span class="sxs-lookup"><span data-stu-id="32ca1-115">When the user interface is run at the Basic or no UI level, the installer handles all the out-of-disk-space logic automatically.</span></span>

<span data-ttu-id="32ca1-116">Quando a interface do usuário é executada no nível completo, o usuário pode receber opções adicionais, como solicitar antes de continuar com uma reversão, desabilitar a reversão ou prosseguir sem reversão quando o disco estiver cheio.</span><span class="sxs-lookup"><span data-stu-id="32ca1-116">When the user interface runs at the Full level, the user can be given additional options, such as prompting before proceeding with a rollback, disabling rollback, or proceeding without rollback when the disk is full.</span></span> <span data-ttu-id="32ca1-117">Cabe ao desenvolvedor do pacote criar a sequência da caixa de diálogo para fornecer as opções apropriadas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="32ca1-117">It is up to the package developer to author the dialog box sequence to provide the appropriate choices to the user.</span></span> <span data-ttu-id="32ca1-118">Os elementos disponíveis para fazer isso são o [EnableRollback ControlEvent,](enablerollback-controlevent.md), a propriedade [**OutOfDiskSpace**](outofdiskspace.md) , a propriedade [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) e a propriedade **PROMPTROLLBACKCOST** .</span><span class="sxs-lookup"><span data-stu-id="32ca1-118">The elements available to do this are the [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property, and the **PROMPTROLLBACKCOST** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ca1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32ca1-119">Requirements</span></span>



| <span data-ttu-id="32ca1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ca1-120">Requirement</span></span> | <span data-ttu-id="32ca1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="32ca1-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32ca1-122">Versão</span><span class="sxs-lookup"><span data-stu-id="32ca1-122">Version</span></span><br/> | <span data-ttu-id="32ca1-123">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="32ca1-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="32ca1-124">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="32ca1-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="32ca1-125">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="32ca1-125">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="32ca1-126">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="32ca1-126">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32ca1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="32ca1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ca1-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="32ca1-128">Properties</span></span>](properties.md)
</dt> </dl>

 

 




