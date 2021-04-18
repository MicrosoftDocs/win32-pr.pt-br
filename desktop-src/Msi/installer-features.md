---
description: A propriedade Features é uma propriedade somente leitura que retorna um objeto StringList que enumera o conjunto de recursos publicados para o produto especificado.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Propriedade Installer. Features
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751649"
---
# <a name="installerfeatures-property"></a><span data-ttu-id="61645-103">Propriedade Installer. Features</span><span class="sxs-lookup"><span data-stu-id="61645-103">Installer.Features property</span></span>

<span data-ttu-id="61645-104">A propriedade **Features** é uma propriedade somente leitura que retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de recursos publicados para o produto especificado.</span><span class="sxs-lookup"><span data-stu-id="61645-104">The **Features** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of published features for the specified product.</span></span>

<span data-ttu-id="61645-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="61645-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61645-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61645-106">Syntax</span></span>


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a><span data-ttu-id="61645-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="61645-107">Property value</span></span>

<span data-ttu-id="61645-108">Especifica o código do produto do produto.</span><span class="sxs-lookup"><span data-stu-id="61645-108">Specifies the product code of the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="61645-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="61645-109">Remarks</span></span>

<span data-ttu-id="61645-110">Para enumerar os recursos, um aplicativo é iterado por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each.</span><span class="sxs-lookup"><span data-stu-id="61645-110">To enumerate the features, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="61645-111">Como os recursos não são ordenados, qualquer recurso novo tem um índice arbitrário, o que significa que a função pode retornar recursos em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="61645-111">Because features are not ordered, any new feature has an arbitrary index, meaning the function can return features in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="61645-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61645-112">Requirements</span></span>



| <span data-ttu-id="61645-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="61645-113">Requirement</span></span> | <span data-ttu-id="61645-114">Valor</span><span class="sxs-lookup"><span data-stu-id="61645-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61645-115">Versão</span><span class="sxs-lookup"><span data-stu-id="61645-115">Version</span></span><br/> | <span data-ttu-id="61645-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="61645-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="61645-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="61645-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="61645-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="61645-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="61645-119">DLL</span><span class="sxs-lookup"><span data-stu-id="61645-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="61645-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61645-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="61645-121">IID</span><span class="sxs-lookup"><span data-stu-id="61645-121">IID</span></span><br/>     | <span data-ttu-id="61645-122">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="61645-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="61645-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="61645-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61645-124">**MsiEnumFeatures**</span><span class="sxs-lookup"><span data-stu-id="61645-124">**MsiEnumFeatures**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[<span data-ttu-id="61645-125">Funções de status do sistema</span><span class="sxs-lookup"><span data-stu-id="61645-125">System Status Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




