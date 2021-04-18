---
description: A propriedade patches somente leitura do objeto instalador retorna um objeto StringList que contém todos os patches aplicados ao produto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Propriedade Installer. patches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752037"
---
# <a name="installerpatches-property"></a><span data-ttu-id="08c05-103">Propriedade Installer. patches</span><span class="sxs-lookup"><span data-stu-id="08c05-103">Installer.Patches property</span></span>

<span data-ttu-id="08c05-104">A propriedade **patches** somente leitura do objeto [**instalador**](installer-object.md) retorna um objeto [**StringList**](stringlist-object.md) que contém todos os patches aplicados ao produto.</span><span class="sxs-lookup"><span data-stu-id="08c05-104">The read-only **Patches** property of the [**Installer**](installer-object.md) object returns a [**StringList**](stringlist-object.md) object that contains all the patches applied to the product.</span></span>

<span data-ttu-id="08c05-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="08c05-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c05-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08c05-106">Syntax</span></span>


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a><span data-ttu-id="08c05-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="08c05-107">Property value</span></span>

<span data-ttu-id="08c05-108">Especifica o código do produto.</span><span class="sxs-lookup"><span data-stu-id="08c05-108">Specifies the product code.</span></span>

## <a name="remarks"></a><span data-ttu-id="08c05-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="08c05-109">Remarks</span></span>

<span data-ttu-id="08c05-110">Para enumerar os patches, um aplicativo é iterado por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each.</span><span class="sxs-lookup"><span data-stu-id="08c05-110">To enumerate the patches, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="08c05-111">Como os patches não são ordenados, qualquer patch novo tem um índice arbitrário.</span><span class="sxs-lookup"><span data-stu-id="08c05-111">Because patches are not ordered, any new patch has an arbitrary index.</span></span> <span data-ttu-id="08c05-112">Isso significa que a função pode retornar patches em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="08c05-112">This means that the function can return patches in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c05-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08c05-113">Requirements</span></span>



| <span data-ttu-id="08c05-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="08c05-114">Requirement</span></span> | <span data-ttu-id="08c05-115">Valor</span><span class="sxs-lookup"><span data-stu-id="08c05-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c05-116">Versão</span><span class="sxs-lookup"><span data-stu-id="08c05-116">Version</span></span><br/> | <span data-ttu-id="08c05-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="08c05-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="08c05-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08c05-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="08c05-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="08c05-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="08c05-120">DLL</span><span class="sxs-lookup"><span data-stu-id="08c05-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="08c05-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08c05-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="08c05-122">IID</span><span class="sxs-lookup"><span data-stu-id="08c05-122">IID</span></span><br/>     | <span data-ttu-id="08c05-123">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="08c05-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="08c05-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="08c05-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c05-125">**MsiEnumPatches**</span><span class="sxs-lookup"><span data-stu-id="08c05-125">**MsiEnumPatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




