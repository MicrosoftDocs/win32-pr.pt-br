---
description: A propriedade componentes somente leitura retorna um objeto StringList que enumera o conjunto de componentes instalados para todos os produtos.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Propriedade Installer. Components
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751651"
---
# <a name="installercomponents-property"></a><span data-ttu-id="f11e6-103">Propriedade Installer. Components</span><span class="sxs-lookup"><span data-stu-id="f11e6-103">Installer.Components property</span></span>

<span data-ttu-id="f11e6-104">A propriedade **componentes** somente leitura retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de componentes instalados para todos os produtos.</span><span class="sxs-lookup"><span data-stu-id="f11e6-104">The read-only **Components** property returns a [**StringList**](stringlist-object.md) object enumerating the set of installed components for all products.</span></span>

<span data-ttu-id="f11e6-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="f11e6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11e6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f11e6-106">Syntax</span></span>


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a><span data-ttu-id="f11e6-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f11e6-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f11e6-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="f11e6-108">Remarks</span></span>

<span data-ttu-id="f11e6-109">Para enumerar os componentes, um aplicativo pode iterar por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each.</span><span class="sxs-lookup"><span data-stu-id="f11e6-109">To enumerate the components, an application can iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="f11e6-110">Como os componentes não são ordenados, todos os componentes novos têm um índice arbitrário.</span><span class="sxs-lookup"><span data-stu-id="f11e6-110">Because components are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="f11e6-111">Isso significa que a função pode retornar componentes em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="f11e6-111">This means that the function can return components in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="f11e6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f11e6-112">Requirements</span></span>



| <span data-ttu-id="f11e6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f11e6-113">Requirement</span></span> | <span data-ttu-id="f11e6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f11e6-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f11e6-115">Versão</span><span class="sxs-lookup"><span data-stu-id="f11e6-115">Version</span></span><br/> | <span data-ttu-id="f11e6-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f11e6-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f11e6-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f11e6-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f11e6-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f11e6-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f11e6-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f11e6-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="f11e6-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f11e6-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f11e6-121">IID</span><span class="sxs-lookup"><span data-stu-id="f11e6-121">IID</span></span><br/>     | <span data-ttu-id="f11e6-122">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f11e6-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="f11e6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f11e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f11e6-124">**MsiEnumComponents**</span><span class="sxs-lookup"><span data-stu-id="f11e6-124">**MsiEnumComponents**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




