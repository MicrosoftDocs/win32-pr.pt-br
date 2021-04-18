---
description: A propriedade MsiNetAssemblySupport indica se o computador dá suporte a assemblies de tempo de execução de idioma comum.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Propriedade MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751848"
---
# <a name="msinetassemblysupport-property"></a><span data-ttu-id="a8494-103">Propriedade MsiNetAssemblySupport</span><span class="sxs-lookup"><span data-stu-id="a8494-103">MsiNetAssemblySupport property</span></span>

<span data-ttu-id="a8494-104">A propriedade **MsiNetAssemblySupport** indica se o computador dá suporte a assemblies de tempo de execução de idioma comum.</span><span class="sxs-lookup"><span data-stu-id="a8494-104">The **MsiNetAssemblySupport** property indicates whether the computer supports common language run-time assemblies.</span></span> <span data-ttu-id="a8494-105">Em sistemas que oferecem suporte a assemblies de tempo de execução de idioma comum, o instalador define o valor de **MsiNetAssemblySupport** para a versão de arquivo de Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="a8494-105">On systems that support common language run-time assemblies, the installer sets the value of **MsiNetAssemblySupport** to the file version of Fusion.dll.</span></span> <span data-ttu-id="a8494-106">O instalador não definirá essa propriedade se o sistema operacional não oferecer suporte a assemblies de tempo de execução de idioma comum.</span><span class="sxs-lookup"><span data-stu-id="a8494-106">The installer does not set this property if the operating system does not support common language run-time assemblies.</span></span> <span data-ttu-id="a8494-107">Quando várias versões do Fusion.dll são instaladas lado a lado no computador do usuário, essa propriedade é definida como a versão mais recente do arquivo de Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="a8494-107">When multiple versions of Fusion.dll are installed side-by-side on the user's computer, this property is set to the latest version of the Fusion.dll file.</span></span> <span data-ttu-id="a8494-108">Por exemplo, se .NET Framework versão 1.0.3705 (Fusion.dll versão 1.0.3705.15) e .NET Framework versão 1.1.4322 (Fusion.dll versão 1.1.4322.314) forem instaladas lado a lado, a propriedade **MsiNetAssemblySupport** será definida como 1.1.4322.314.</span><span class="sxs-lookup"><span data-stu-id="a8494-108">For example, if .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15)and .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) are installed side-by-side, the **MsiNetAssemblySupport** property is set to 1.1.4322.314.</span></span> <span data-ttu-id="a8494-109">Para obter mais informações, consulte [assemblies](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a8494-109">For more information, see [Assemblies](assemblies.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8494-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8494-110">Requirements</span></span>



| <span data-ttu-id="a8494-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8494-111">Requirement</span></span> | <span data-ttu-id="a8494-112">Valor</span><span class="sxs-lookup"><span data-stu-id="a8494-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8494-113">Versão</span><span class="sxs-lookup"><span data-stu-id="a8494-113">Version</span></span><br/> | <span data-ttu-id="a8494-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8494-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a8494-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a8494-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a8494-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8494-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a8494-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a8494-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8494-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8494-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8494-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8494-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




