---
description: Retorna um objeto Recordlist que enumera a lista de produtos.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Propriedade Installer. ProductsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748154"
---
# <a name="installerproductsex-property"></a><span data-ttu-id="5b161-103">Propriedade Installer. ProductsEx</span><span class="sxs-lookup"><span data-stu-id="5b161-103">Installer.ProductsEx property</span></span>

<span data-ttu-id="5b161-104">A propriedade **ProductsEx** retorna um objeto [**recordlist**](recordlist-object.md) que enumera a lista de produtos.</span><span class="sxs-lookup"><span data-stu-id="5b161-104">The **ProductsEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of products.</span></span> <span data-ttu-id="5b161-105">Essa propriedade chama [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span><span class="sxs-lookup"><span data-stu-id="5b161-105">This property calls [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span></span>

<span data-ttu-id="5b161-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5b161-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b161-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b161-107">Syntax</span></span>


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a><span data-ttu-id="5b161-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5b161-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="5b161-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b161-109">Requirements</span></span>



| <span data-ttu-id="5b161-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b161-110">Requirement</span></span> | <span data-ttu-id="5b161-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5b161-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b161-112">Versão</span><span class="sxs-lookup"><span data-stu-id="5b161-112">Version</span></span><br/> | <span data-ttu-id="5b161-113">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b161-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5b161-114">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5b161-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5b161-115">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b161-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="5b161-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5b161-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b161-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b161-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="5b161-118">IID</span><span class="sxs-lookup"><span data-stu-id="5b161-118">IID</span></span><br/>     | <span data-ttu-id="5b161-119">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5b161-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="5b161-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b161-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b161-121">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="5b161-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="5b161-122">**MsiEnumProductsEx**</span><span class="sxs-lookup"><span data-stu-id="5b161-122">**MsiEnumProductsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="5b161-123">**Produto**</span><span class="sxs-lookup"><span data-stu-id="5b161-123">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="5b161-124">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="5b161-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




