---
description: O instalador define a propriedade AFTERREBOOT como 1 após uma reinicialização invocada pela ação ForceReboot. O instalador adiciona AFTERREBOOT = 1 à linha de comando executar imediatamente após a reinicialização.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: Propriedade AFTERREBOOT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752467"
---
# <a name="afterreboot-property"></a><span data-ttu-id="41f08-104">Propriedade AFTERREBOOT</span><span class="sxs-lookup"><span data-stu-id="41f08-104">AFTERREBOOT property</span></span>

<span data-ttu-id="41f08-105">O instalador define a propriedade **AFTERREBOOT** como 1 após uma reinicialização invocada pela [ação ForceReboot](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="41f08-105">The installer sets the **AFTERREBOOT** property to 1 after a reboot invoked by the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="41f08-106">O instalador adiciona AFTERREBOOT = 1 à linha de comando executar imediatamente após a reinicialização.</span><span class="sxs-lookup"><span data-stu-id="41f08-106">The installer adds AFTERREBOOT=1 to the command line run immediately after the reboot.</span></span>

## <a name="remarks"></a><span data-ttu-id="41f08-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="41f08-107">Remarks</span></span>

<span data-ttu-id="41f08-108">A [ação ForceReboot](forcereboot-action.md) sempre deve ser usada com uma instrução condicional, de modo que o instalador disparará uma reinicialização somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="41f08-108">The [ForceReboot action](forcereboot-action.md) must always be used with a conditional statement such that the installer triggers a reboot only when necessary.</span></span> <span data-ttu-id="41f08-109">Uma reinicialização poderá ser necessária se um determinado arquivo tiver sido substituído ou um componente específico tiver sido instalado.</span><span class="sxs-lookup"><span data-stu-id="41f08-109">A reboot might be required if a particular file was replaced or a particular component was installed.</span></span> <span data-ttu-id="41f08-110">O caso é diferente para cada produto e uma ação personalizada pode ser necessária para determinar se uma reinicialização é necessária.</span><span class="sxs-lookup"><span data-stu-id="41f08-110">The case is different for each product and a custom action might be needed to determine whether a reboot is needed.</span></span> <span data-ttu-id="41f08-111">A condição na ação ForceReboot normalmente usa a propriedade **AFTERREBOOT** .</span><span class="sxs-lookup"><span data-stu-id="41f08-111">The condition on the ForceReboot action commonly makes use of the **AFTERREBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f08-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41f08-112">Requirements</span></span>



| <span data-ttu-id="41f08-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="41f08-113">Requirement</span></span> | <span data-ttu-id="41f08-114">Valor</span><span class="sxs-lookup"><span data-stu-id="41f08-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f08-115">Versão</span><span class="sxs-lookup"><span data-stu-id="41f08-115">Version</span></span><br/> | <span data-ttu-id="41f08-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="41f08-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="41f08-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="41f08-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="41f08-118">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="41f08-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="41f08-119">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="41f08-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41f08-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="41f08-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f08-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41f08-121">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="41f08-122">Reinicializações do sistema</span><span class="sxs-lookup"><span data-stu-id="41f08-122">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




