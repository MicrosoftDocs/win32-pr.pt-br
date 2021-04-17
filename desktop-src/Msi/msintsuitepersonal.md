---
description: No Windows XP e sistemas operacionais posteriores, o instalador definirá a propriedade MsiNTSuitePersonal como 1 se o sistema operacional for o Windows XP Home Edition.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Propriedade MsiNTSuitePersonal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747754"
---
# <a name="msintsuitepersonal-property"></a><span data-ttu-id="38a65-103">Propriedade MsiNTSuitePersonal</span><span class="sxs-lookup"><span data-stu-id="38a65-103">MsiNTSuitePersonal property</span></span>

<span data-ttu-id="38a65-104">No Windows XP e sistemas operacionais posteriores, o instalador definirá a propriedade **MsiNTSuitePersonal** como 1 se o sistema operacional for o Windows XP Home Edition.</span><span class="sxs-lookup"><span data-stu-id="38a65-104">On Windows XP and later operating systems, the installer sets the **MsiNTSuitePersonal** property to 1 if the operating system is Windows XP Home Edition.</span></span> <span data-ttu-id="38a65-105">O instalador definirá essa propriedade como 1 somente se o \_ sinalizador pessoal do pacote de ver \_ estiver definido na estrutura [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="38a65-105">The installer sets this property to 1 only if the VER\_SUITE\_PERSONAL flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="38a65-106">Caso contrário, o instalador não definirá essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="38a65-106">Otherwise the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="38a65-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38a65-107">Requirements</span></span>



| <span data-ttu-id="38a65-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="38a65-108">Requirement</span></span> | <span data-ttu-id="38a65-109">Valor</span><span class="sxs-lookup"><span data-stu-id="38a65-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38a65-110">Versão</span><span class="sxs-lookup"><span data-stu-id="38a65-110">Version</span></span><br/> | <span data-ttu-id="38a65-111">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38a65-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="38a65-112">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="38a65-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="38a65-113">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="38a65-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="38a65-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="38a65-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38a65-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="38a65-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a65-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="38a65-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
