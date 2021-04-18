---
description: A propriedade MSIPATCHREMOVE especifica a lista de patches a serem removidos durante uma instalação.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Propriedade MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780950"
---
# <a name="msipatchremove-property"></a><span data-ttu-id="abeb4-103">Propriedade MSIPATCHREMOVE</span><span class="sxs-lookup"><span data-stu-id="abeb4-103">MSIPATCHREMOVE property</span></span>

<span data-ttu-id="abeb4-104">A propriedade **MSIPATCHREMOVE** especifica a lista de patches a serem removidos durante uma instalação.</span><span class="sxs-lookup"><span data-stu-id="abeb4-104">The **MSIPATCHREMOVE** property specifies the list of patches to remove during an installation.</span></span> <span data-ttu-id="abeb4-105">Os patches individuais na lista são separados por ponto e vírgula e podem ser representados pelo GUID de código de patch ou pelo caminho completo para o patch.</span><span class="sxs-lookup"><span data-stu-id="abeb4-105">Individual patches in the list are separated by semicolons and can be represented by patch code GUID or the full path to the patch.</span></span> <span data-ttu-id="abeb4-106">A função [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) e o método [**RemovePatches**](installer-removepatches.md) do objeto [instalador](installer-object.md) definem a propriedade **MSIPATCHREMOVE** .</span><span class="sxs-lookup"><span data-stu-id="abeb4-106">The [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function and the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object set the **MSIPATCHREMOVE** property.</span></span>

<span data-ttu-id="abeb4-107">A propriedade **MSIPATCHREMOVE** pode ser definida na linha de comando da seguinte maneira para remover um patch.</span><span class="sxs-lookup"><span data-stu-id="abeb4-107">The **MSIPATCHREMOVE** property can be set on the command line as follows to remove a patch.</span></span>

<span data-ttu-id="abeb4-108">**msiexec/i A: \\Example.msi MSIPATCHREMOVE = c: \\ patches \\ qfe1. msp; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**</span><span class="sxs-lookup"><span data-stu-id="abeb4-108">**msiexec /i A:\\Example.msi MSIPATCHREMOVE=c:\\patches\\qfe1.msp;{0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**</span></span>

## <a name="requirements"></a><span data-ttu-id="abeb4-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abeb4-109">Requirements</span></span>



| <span data-ttu-id="abeb4-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="abeb4-110">Requirement</span></span> | <span data-ttu-id="abeb4-111">Valor</span><span class="sxs-lookup"><span data-stu-id="abeb4-111">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abeb4-112">Versão</span><span class="sxs-lookup"><span data-stu-id="abeb4-112">Version</span></span><br/> | <span data-ttu-id="abeb4-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="abeb4-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="abeb4-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="abeb4-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="abeb4-115">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="abeb4-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="abeb4-116">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="abeb4-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="abeb4-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="abeb4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abeb4-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="abeb4-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="abeb4-119">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="abeb4-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




