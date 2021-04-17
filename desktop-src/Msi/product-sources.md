---
description: A propriedade sources enumera todas as fontes para a instância do produto.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Propriedade Product. Sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770182"
---
# <a name="productsources-property"></a><span data-ttu-id="3febe-103">Propriedade Product. Sources</span><span class="sxs-lookup"><span data-stu-id="3febe-103">Product.Sources property</span></span>

<span data-ttu-id="3febe-104">A propriedade **sources** enumera todas as fontes para a instância do produto.</span><span class="sxs-lookup"><span data-stu-id="3febe-104">The **Sources** property enumerates all the sources for the product instance.</span></span> <span data-ttu-id="3febe-105">Essa propriedade chama [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) e retorna a matriz de cadeias de caracteres e aceita o tipo de origem como argumento.</span><span class="sxs-lookup"><span data-stu-id="3febe-105">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns the array of strings, and accepts the source type as argument.</span></span> <span data-ttu-id="3febe-106">O tipo de origem pode ser MSISOURCETYPE \_ Network ou MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="3febe-106">The source type can be MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

<span data-ttu-id="3febe-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3febe-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3febe-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3febe-108">Syntax</span></span>


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a><span data-ttu-id="3febe-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3febe-109">Property value</span></span>

<span data-ttu-id="3febe-110">O tipo de origem a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="3febe-110">The type of source to enumerate.</span></span> <span data-ttu-id="3febe-111">O valor pode ser *msiInstallSourceTypeNetwork* (1) ou *msiInstallSourceTypeURL* (2).</span><span class="sxs-lookup"><span data-stu-id="3febe-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="3febe-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3febe-112">Requirements</span></span>



| <span data-ttu-id="3febe-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3febe-113">Requirement</span></span> | <span data-ttu-id="3febe-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3febe-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3febe-115">Versão</span><span class="sxs-lookup"><span data-stu-id="3febe-115">Version</span></span><br/> | <span data-ttu-id="3febe-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3febe-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3febe-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3febe-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3febe-118">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3febe-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="3febe-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3febe-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="3febe-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3febe-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="3febe-121">IID</span><span class="sxs-lookup"><span data-stu-id="3febe-121">IID</span></span><br/>     | <span data-ttu-id="3febe-122">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3febe-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="3febe-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3febe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3febe-124">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="3febe-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="3febe-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="3febe-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="3febe-126">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="3febe-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




