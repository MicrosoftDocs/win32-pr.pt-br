---
description: A propriedade RelatedProducts somente leitura retorna um objeto StringList que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário atual e computador com uma propriedade UpgradeCode especificada em sua tabela de propriedades.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Propriedade Installer. RelatedProducts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749996"
---
# <a name="installerrelatedproducts-property"></a><span data-ttu-id="20418-103">Propriedade Installer. RelatedProducts</span><span class="sxs-lookup"><span data-stu-id="20418-103">Installer.RelatedProducts property</span></span>

<span data-ttu-id="20418-104">A propriedade **RelatedProducts** somente leitura retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário atual e computador com uma propriedade [**UpgradeCode**](upgradecode.md) especificada em sua [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="20418-104">The read-only **RelatedProducts** property returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine with a specified [**UpgradeCode**](upgradecode.md) property in their [Property table](property-table.md).</span></span>

<span data-ttu-id="20418-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="20418-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="20418-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20418-106">Syntax</span></span>


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a><span data-ttu-id="20418-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="20418-107">Property value</span></span>

<span data-ttu-id="20418-108">O código de atualização de produtos relacionados que o instalador enumera.</span><span class="sxs-lookup"><span data-stu-id="20418-108">The upgrade code of related products that the installer enumerates.</span></span>

## <a name="remarks"></a><span data-ttu-id="20418-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="20418-109">Remarks</span></span>

<span data-ttu-id="20418-110">Para enumerar os produtos relacionados, um aplicativo é iterado por meio da [**StringList**](stringlist-object.md) usando uma construção for each.</span><span class="sxs-lookup"><span data-stu-id="20418-110">To enumerate the related products, an application iterates through the [**StringList**](stringlist-object.md) using a For Each construct.</span></span> <span data-ttu-id="20418-111">Como os produtos relacionados não são ordenados, qualquer produto relacionado novo tem um índice arbitrário.</span><span class="sxs-lookup"><span data-stu-id="20418-111">Because related products are not ordered, any new related product has an arbitrary index.</span></span> <span data-ttu-id="20418-112">Isso significa que a função pode retornar produtos relacionados em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="20418-112">This means that the function can return related products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="20418-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20418-113">Requirements</span></span>



| <span data-ttu-id="20418-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="20418-114">Requirement</span></span> | <span data-ttu-id="20418-115">Valor</span><span class="sxs-lookup"><span data-stu-id="20418-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20418-116">Versão</span><span class="sxs-lookup"><span data-stu-id="20418-116">Version</span></span><br/> | <span data-ttu-id="20418-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20418-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="20418-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20418-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="20418-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="20418-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="20418-120">DLL</span><span class="sxs-lookup"><span data-stu-id="20418-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="20418-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20418-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="20418-122">IID</span><span class="sxs-lookup"><span data-stu-id="20418-122">IID</span></span><br/>     | <span data-ttu-id="20418-123">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="20418-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="20418-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="20418-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20418-125">**MsiEnumRelatedProducts**</span><span class="sxs-lookup"><span data-stu-id="20418-125">**MsiEnumRelatedProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




