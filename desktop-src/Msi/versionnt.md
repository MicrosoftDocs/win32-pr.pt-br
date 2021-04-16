---
description: O instalador define a propriedade VersionNT para o número de versão do sistema operacional, indefinido se o sistema operacional não for Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 ou Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Propriedade VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752435"
---
# <a name="versionnt-property"></a><span data-ttu-id="52795-103">Propriedade VersionNT</span><span class="sxs-lookup"><span data-stu-id="52795-103">VersionNT property</span></span>

<span data-ttu-id="52795-104">O instalador define a propriedade **VersionNT** para o número de versão do sistema operacional, indefinido se o sistema operacional não for Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52795-104">The installer sets the **VersionNT** property to the version number for the operating system, undefined if the operating system is not Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008, or Windows 7.</span></span> <span data-ttu-id="52795-105">O valor é um inteiro: MajorVersion \* 100 + MinorVersion.</span><span class="sxs-lookup"><span data-stu-id="52795-105">The value is an integer: MajorVersion \* 100 + MinorVersion.</span></span>

<span data-ttu-id="52795-106">Instruções condicionais que dependem do sistema operacional podem usar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="52795-106">Conditional statements that depend upon the operating system can use this property.</span></span>

<span data-ttu-id="52795-107">Consulte também [valores de Propriedade do sistema operacional](operating-system-property-values.md).</span><span class="sxs-lookup"><span data-stu-id="52795-107">See also [Operating System Property Values](operating-system-property-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52795-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="52795-108">Remarks</span></span>

<span data-ttu-id="52795-109">As expressões de condição podem testar o Windows NT, o Windows 2000 ou o Windows XP usando o nome da propriedade, ou podem verificar a versão usando um operador de comparação.</span><span class="sxs-lookup"><span data-stu-id="52795-109">Condition expressions can test for Windows NT, Windows 2000, or Windows XP by using the property name, or may verify the version by using a comparison operator.</span></span>

## <a name="requirements"></a><span data-ttu-id="52795-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52795-110">Requirements</span></span>



| <span data-ttu-id="52795-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="52795-111">Requirement</span></span> | <span data-ttu-id="52795-112">Valor</span><span class="sxs-lookup"><span data-stu-id="52795-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52795-113">Versão</span><span class="sxs-lookup"><span data-stu-id="52795-113">Version</span></span><br/> | <span data-ttu-id="52795-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52795-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="52795-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52795-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="52795-116">Windows Installer no Windows Server 2003 ou no Windows XP, consulte os [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="52795-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52795-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="52795-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52795-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="52795-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




