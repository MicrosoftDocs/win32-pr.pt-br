---
description: A propriedade PatchFiles retorna um objeto StringList que contém uma lista de arquivos que podem ser atualizados pela lista de patches fornecida.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Propriedade Installer. PatchFiles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752451"
---
# <a name="installerpatchfiles-property"></a><span data-ttu-id="35ea1-103">Propriedade Installer. PatchFiles</span><span class="sxs-lookup"><span data-stu-id="35ea1-103">Installer.PatchFiles property</span></span>

<span data-ttu-id="35ea1-104">A propriedade **PatchFiles** retorna um objeto [**StringList**](stringlist-object.md) que contém uma lista de arquivos que podem ser atualizados pela lista de patches fornecida.</span><span class="sxs-lookup"><span data-stu-id="35ea1-104">The **PatchFiles** property returns a [**StringList**](stringlist-object.md) object that contains a list of files that can be updated by the provided list of patches.</span></span> <span data-ttu-id="35ea1-105">Essa propriedade chama [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span><span class="sxs-lookup"><span data-stu-id="35ea1-105">This property calls [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="35ea1-106">Para obter mais informações sobre como usar a propriedade **PatchFiles** , consulte [listando os arquivos que podem ser atualizados](listing-the-files-that-can-be-updated.md).</span><span class="sxs-lookup"><span data-stu-id="35ea1-106">For more information about using the **PatchFiles** property see [Listing the Files that can be Updated](listing-the-files-that-can-be-updated.md).</span></span>

<span data-ttu-id="35ea1-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="35ea1-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ea1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35ea1-108">Syntax</span></span>


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a><span data-ttu-id="35ea1-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="35ea1-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="35ea1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ea1-110">Requirements</span></span>



| <span data-ttu-id="35ea1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ea1-111">Requirement</span></span> | <span data-ttu-id="35ea1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="35ea1-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ea1-113">Versão</span><span class="sxs-lookup"><span data-stu-id="35ea1-113">Version</span></span><br/> | <span data-ttu-id="35ea1-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="35ea1-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="35ea1-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="35ea1-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="35ea1-116">Windows Installer 4,5 no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="35ea1-116">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="35ea1-117">DLL</span><span class="sxs-lookup"><span data-stu-id="35ea1-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="35ea1-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35ea1-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="35ea1-119">IID</span><span class="sxs-lookup"><span data-stu-id="35ea1-119">IID</span></span><br/>     | <span data-ttu-id="35ea1-120">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="35ea1-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="35ea1-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="35ea1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ea1-122">**Objeto do instalador**</span><span class="sxs-lookup"><span data-stu-id="35ea1-122">**Installer Object**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="35ea1-123">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="35ea1-123">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




