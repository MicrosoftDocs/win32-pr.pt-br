---
description: O instalador define a propriedade TempFolder como o caminho completo para a pasta Temp. Os autores não devem precisar definir a propriedade TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Propriedade TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752632"
---
# <a name="tempfolder-property"></a><span data-ttu-id="426ee-103">Propriedade TempFolder</span><span class="sxs-lookup"><span data-stu-id="426ee-103">TempFolder property</span></span>

<span data-ttu-id="426ee-104">O instalador define a propriedade **TempFolder** como o caminho completo para a pasta Temp.</span><span class="sxs-lookup"><span data-stu-id="426ee-104">The installer sets the **TempFolder** property to the full path to the Temp folder.</span></span>

<span data-ttu-id="426ee-105">Os autores não devem precisar definir a propriedade **TempFolder** .</span><span class="sxs-lookup"><span data-stu-id="426ee-105">Authors should not need to set the **TempFolder** property.</span></span> <span data-ttu-id="426ee-106">Windows Installer usa a função [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) para recuperar o caminho do diretório designado para arquivos temporários e para definir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="426ee-106">Windows Installer uses the [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files and to set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="426ee-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="426ee-107">Remarks</span></span>

<span data-ttu-id="426ee-108">Um valor comum para essa propriedade é C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="426ee-108">A common value for this property is C:\\Temp.</span></span>

## <a name="requirements"></a><span data-ttu-id="426ee-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="426ee-109">Requirements</span></span>



| <span data-ttu-id="426ee-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="426ee-110">Requirement</span></span> | <span data-ttu-id="426ee-111">Valor</span><span class="sxs-lookup"><span data-stu-id="426ee-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="426ee-112">Versão</span><span class="sxs-lookup"><span data-stu-id="426ee-112">Version</span></span><br/> | <span data-ttu-id="426ee-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="426ee-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="426ee-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="426ee-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="426ee-115">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="426ee-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="426ee-116">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="426ee-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="426ee-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="426ee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="426ee-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="426ee-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 
