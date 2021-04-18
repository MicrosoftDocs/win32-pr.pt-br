---
description: A propriedade ShortcutTarget do objeto do instalador examina um atalho e retorna seu produto, o nome do recurso e o componente, se disponível.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Propriedade Installer. ShortcutTarget
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752249"
---
# <a name="installershortcuttarget-property"></a><span data-ttu-id="da128-103">Propriedade Installer. ShortcutTarget</span><span class="sxs-lookup"><span data-stu-id="da128-103">Installer.ShortcutTarget property</span></span>

<span data-ttu-id="da128-104">A propriedade **ShortcutTarget** do objeto do [**instalador**](installer-object.md) examina um atalho e retorna seu produto, o nome do recurso e o componente, se disponível.</span><span class="sxs-lookup"><span data-stu-id="da128-104">The **ShortcutTarget** property of the [**Installer**](installer-object.md) object examines a shortcut and returns its product, feature name, and component if available.</span></span>

<span data-ttu-id="da128-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="da128-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da128-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da128-106">Syntax</span></span>


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a><span data-ttu-id="da128-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="da128-107">Property value</span></span>

<span data-ttu-id="da128-108">Caminho completo e nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="da128-108">Full path and file name for the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="da128-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="da128-109">Remarks</span></span>

<span data-ttu-id="da128-110">ShortcutTarget retorna um [**objeto de registro**](record-object.md) que contém três campos:</span><span class="sxs-lookup"><span data-stu-id="da128-110">ShortcutTarget returns a [**Record object**](record-object.md) that contains three fields:</span></span>

-   <span data-ttu-id="da128-111">O campo 1 é um GUID para o código do produto do atalho, se disponível.</span><span class="sxs-lookup"><span data-stu-id="da128-111">Field 1 is a GUID for the product code of the shortcut, if available.</span></span> <span data-ttu-id="da128-112">Este campo pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="da128-112">This field can be null.</span></span>
-   <span data-ttu-id="da128-113">O campo 2 é a ID do recurso do atalho, se disponível.</span><span class="sxs-lookup"><span data-stu-id="da128-113">Field 2 is the Feature ID of the shortcut, if available.</span></span> <span data-ttu-id="da128-114">Este campo pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="da128-114">This field can be null.</span></span>
-   <span data-ttu-id="da128-115">O campo 3 é um GUID para o código do componente, se disponível.</span><span class="sxs-lookup"><span data-stu-id="da128-115">Field 3 is a GUID for the component code, if available.</span></span> <span data-ttu-id="da128-116">Este campo pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="da128-116">This field can be null.</span></span>

## <a name="requirements"></a><span data-ttu-id="da128-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da128-117">Requirements</span></span>



| <span data-ttu-id="da128-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="da128-118">Requirement</span></span> | <span data-ttu-id="da128-119">Valor</span><span class="sxs-lookup"><span data-stu-id="da128-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da128-120">Versão</span><span class="sxs-lookup"><span data-stu-id="da128-120">Version</span></span><br/> | <span data-ttu-id="da128-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="da128-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="da128-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="da128-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="da128-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="da128-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="da128-124">DLL</span><span class="sxs-lookup"><span data-stu-id="da128-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="da128-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da128-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="da128-126">IID</span><span class="sxs-lookup"><span data-stu-id="da128-126">IID</span></span><br/>     | <span data-ttu-id="da128-127">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="da128-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="da128-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="da128-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da128-129">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="da128-129">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[<span data-ttu-id="da128-130">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="da128-130">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




