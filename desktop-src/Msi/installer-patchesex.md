---
description: A propriedade PatchesEx retorna um objeto Recordlist que enumera a lista de patches.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Propriedade Installer. PatchesEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747968"
---
# <a name="installerpatchesex-property"></a><span data-ttu-id="b6e2b-103">Propriedade Installer. PatchesEx</span><span class="sxs-lookup"><span data-stu-id="b6e2b-103">Installer.PatchesEx property</span></span>

<span data-ttu-id="b6e2b-104">A propriedade **PatchesEx** retorna um objeto [**recordlist**](recordlist-object.md) que enumera a lista de patches.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-104">The **PatchesEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of patches.</span></span> <span data-ttu-id="b6e2b-105">Essa propriedade chama [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="b6e2b-105">This property calls [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span>

<span data-ttu-id="b6e2b-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e2b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6e2b-107">Syntax</span></span>


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a><span data-ttu-id="b6e2b-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b6e2b-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e2b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6e2b-109">Requirements</span></span>



| <span data-ttu-id="b6e2b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e2b-110">Requirement</span></span> | <span data-ttu-id="b6e2b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b6e2b-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e2b-112">Versão</span><span class="sxs-lookup"><span data-stu-id="b6e2b-112">Version</span></span><br/> | <span data-ttu-id="b6e2b-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b6e2b-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b6e2b-115">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b6e2b-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="b6e2b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="b6e2b-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="b6e2b-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6e2b-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="b6e2b-118">IID</span><span class="sxs-lookup"><span data-stu-id="b6e2b-118">IID</span></span><br/>     | <span data-ttu-id="b6e2b-119">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b6e2b-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="b6e2b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6e2b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e2b-121">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="b6e2b-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="b6e2b-122">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="b6e2b-122">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="b6e2b-123">**Patch**</span><span class="sxs-lookup"><span data-stu-id="b6e2b-123">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="b6e2b-124">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="b6e2b-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




