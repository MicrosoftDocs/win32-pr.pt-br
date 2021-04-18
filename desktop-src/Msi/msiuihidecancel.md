---
description: Essa propriedade Windows Installer indica quando o nível da interface do usuário interna foi definido para ocultar o botão Cancelar.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Propriedade MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768726"
---
# <a name="msiuihidecancel-property"></a><span data-ttu-id="c102a-103">Propriedade MsiUIHideCancel</span><span class="sxs-lookup"><span data-stu-id="c102a-103">MsiUIHideCancel property</span></span>

<span data-ttu-id="c102a-104">O instalador define a propriedade **MsiUIHideCancel** como 1 quando o nível da interface do usuário interna tiver sido definido para incluir INSTALLUILEVEL \_ HIDECANCEL com a função [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) ou a propriedade [UILevel](installer-uilevel.md)do objeto do [**instalador**](installer-object.md) ou usando opções de [linha de comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="c102a-104">The installer sets the **MsiUIHideCancel** property to 1 when the internal user interface level has been set to include INSTALLUILEVEL\_HIDECANCEL with the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function or the [UILevel](installer-uilevel.md)property of the [**Installer**](installer-object.md) object or by using [Command Line Options](command-line-options.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c102a-105">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c102a-105">Requirements</span></span>



| <span data-ttu-id="c102a-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="c102a-106">Requirement</span></span> | <span data-ttu-id="c102a-107">Valor</span><span class="sxs-lookup"><span data-stu-id="c102a-107">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c102a-108">Versão</span><span class="sxs-lookup"><span data-stu-id="c102a-108">Version</span></span><br/> | <span data-ttu-id="c102a-109">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c102a-109">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c102a-110">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c102a-110">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c102a-111">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c102a-111">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c102a-112">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c102a-112">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c102a-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="c102a-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c102a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c102a-114">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="c102a-115">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="c102a-115">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




