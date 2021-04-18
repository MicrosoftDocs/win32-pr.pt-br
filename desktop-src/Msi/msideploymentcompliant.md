---
description: A propriedade MSIDEPLOYMENTCOMPLIANT pode ser definida para indicar ao instalador que o pacote foi criado e testado para estar em conformidade com o UAC (controle de conta de usuário) no Windows Vista.
ms.assetid: 7ee0dc56-bb9d-4a6e-aa3e-ae4c83f583d7
title: Propriedade MSIDEPLOYMENTCOMPLIANT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a965b7dce941a3d651e2f9f32e3d8f4993ded33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752845"
---
# <a name="msideploymentcompliant-property"></a><span data-ttu-id="1dcbf-103">Propriedade MSIDEPLOYMENTCOMPLIANT</span><span class="sxs-lookup"><span data-stu-id="1dcbf-103">MSIDEPLOYMENTCOMPLIANT property</span></span>

<span data-ttu-id="1dcbf-104">A propriedade **MSIDEPLOYMENTCOMPLIANT** pode ser definida para indicar ao instalador que o pacote foi criado e testado para estar em conformidade com o UAC ( [*controle de conta de usuário*](u-gly.md) ) no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1dcbf-104">The **MSIDEPLOYMENTCOMPLIANT** property can be set to indicate to the installer that the package has been authored and tested to comply with [*User Account Control*](u-gly.md) (UAC) in Windows Vista.</span></span> <span data-ttu-id="1dcbf-105">Se essa propriedade não for definida, o instalador determinará se o pacote está em conformidade com o UAC no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1dcbf-105">If this property is not set, the installer will determine whether the package complies with UAC on Windows Vista.</span></span>

<span data-ttu-id="1dcbf-106">Para obter mais informações sobre o UAC e o Windows Installer, consulte [usando o Windows Installer com o UAC](using-windows-installer-with-uac.md) e [diretrizes para pacotes](guidelines-for-packages.md).</span><span class="sxs-lookup"><span data-stu-id="1dcbf-106">For more information about UAC and Windows Installer, see [Using Windows Installer with UAC](using-windows-installer-with-uac.md) and [Guidelines for Packages](guidelines-for-packages.md).</span></span>

<span data-ttu-id="1dcbf-107">**Windows Installer 3,1, Windows Installer 3,0 e Windows Installer 2,0:** Esta propriedade é ignorada.</span><span class="sxs-lookup"><span data-stu-id="1dcbf-107">**Windows Installer 3.1, Windows Installer 3.0 and Windows Installer 2.0:** This property is ignored.</span></span> <span data-ttu-id="1dcbf-108">Essa propriedade só é usada pelo Windows Installer 4,0 no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1dcbf-108">This property is only used by Windows Installer 4.0 in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dcbf-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dcbf-109">Requirements</span></span>



| <span data-ttu-id="1dcbf-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dcbf-110">Requirement</span></span> | <span data-ttu-id="1dcbf-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1dcbf-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcbf-112">Versão</span><span class="sxs-lookup"><span data-stu-id="1dcbf-112">Version</span></span><br/> | <span data-ttu-id="1dcbf-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1dcbf-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1dcbf-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1dcbf-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1dcbf-115">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o mínimo Service Pack exigido por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="1dcbf-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1dcbf-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dcbf-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dcbf-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1dcbf-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="1dcbf-118">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="1dcbf-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




