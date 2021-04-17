---
description: A propriedade Products é uma propriedade somente leitura que retorna um objeto StringList que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário e a máquina atuais.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Propriedade Installer. Products
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749585"
---
# <a name="installerproducts-property"></a><span data-ttu-id="63119-103">Propriedade Installer. Products</span><span class="sxs-lookup"><span data-stu-id="63119-103">Installer.Products property</span></span>

<span data-ttu-id="63119-104">A propriedade **Products** é uma propriedade somente leitura que retorna um objeto [**StringList**](stringlist-object.md) que enumera o conjunto de todos os produtos instalados ou anunciados para o usuário e a máquina atuais.</span><span class="sxs-lookup"><span data-stu-id="63119-104">The **Products** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine.</span></span>

<span data-ttu-id="63119-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="63119-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63119-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63119-106">Syntax</span></span>


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a><span data-ttu-id="63119-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="63119-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="63119-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="63119-108">Remarks</span></span>

<span data-ttu-id="63119-109">Para enumerar os produtos, um aplicativo é iterado por meio do objeto [**StringList**](stringlist-object.md) usando uma construção for each.</span><span class="sxs-lookup"><span data-stu-id="63119-109">To enumerate the products, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="63119-110">Como os produtos não são ordenados, qualquer produto novo tem um índice arbitrário.</span><span class="sxs-lookup"><span data-stu-id="63119-110">Because products are not ordered, any new product has an arbitrary index.</span></span> <span data-ttu-id="63119-111">Isso significa que a função pode retornar produtos em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="63119-111">This means that the function can return products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="63119-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63119-112">Requirements</span></span>



| <span data-ttu-id="63119-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="63119-113">Requirement</span></span> | <span data-ttu-id="63119-114">Valor</span><span class="sxs-lookup"><span data-stu-id="63119-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63119-115">Versão</span><span class="sxs-lookup"><span data-stu-id="63119-115">Version</span></span><br/> | <span data-ttu-id="63119-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="63119-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="63119-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="63119-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="63119-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="63119-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="63119-119">DLL</span><span class="sxs-lookup"><span data-stu-id="63119-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="63119-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63119-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="63119-121">IID</span><span class="sxs-lookup"><span data-stu-id="63119-121">IID</span></span><br/>     | <span data-ttu-id="63119-122">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="63119-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="63119-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="63119-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63119-124">**MsiEnumProducts**</span><span class="sxs-lookup"><span data-stu-id="63119-124">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




