---
description: A propriedade ShellAdvtSupport é definida pelo instalador se a interface IShellLink do sistema der suporte à resolução do descritor de instalador.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Propriedade ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789764"
---
# <a name="shelladvtsupport-property"></a><span data-ttu-id="b0430-103">Propriedade ShellAdvtSupport</span><span class="sxs-lookup"><span data-stu-id="b0430-103">ShellAdvtSupport property</span></span>

<span data-ttu-id="b0430-104">A propriedade **ShellAdvtSupport** é definida pelo instalador se a interface [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) do sistema der suporte à resolução do descritor de instalador.</span><span class="sxs-lookup"><span data-stu-id="b0430-104">The **ShellAdvtSupport** property is set by the installer if the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0430-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0430-105">Remarks</span></span>

<span data-ttu-id="b0430-106">Se essa propriedade for definida, a interface [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) do sistema dará suporte à resolução do descritor de instalador.</span><span class="sxs-lookup"><span data-stu-id="b0430-106">If this property is set, the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span> <span data-ttu-id="b0430-107">Isso tem suporte no Windows 2000 e em sistemas que executam o Internet Explorer 4, 1.</span><span class="sxs-lookup"><span data-stu-id="b0430-107">This is supported by Windows 2000 and systems running Internet Explorer 4.01.</span></span> <span data-ttu-id="b0430-108">Se essa propriedade não for definida, o instalador terá o comportamento padrão de criação de recursos não anunciados durante a instalação, seja localmente ou executado a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="b0430-108">If this property is not set, the installer has the default behavior of creating non-advertised features during installation, either locally or run from source.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0430-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0430-109">Requirements</span></span>



| <span data-ttu-id="b0430-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0430-110">Requirement</span></span> | <span data-ttu-id="b0430-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b0430-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0430-112">Versão</span><span class="sxs-lookup"><span data-stu-id="b0430-112">Version</span></span><br/> | <span data-ttu-id="b0430-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b0430-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b0430-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b0430-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b0430-115">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b0430-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b0430-116">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b0430-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0430-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0430-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0430-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0430-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="b0430-119">Suporte de plataforma do anúncio</span><span class="sxs-lookup"><span data-stu-id="b0430-119">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 
