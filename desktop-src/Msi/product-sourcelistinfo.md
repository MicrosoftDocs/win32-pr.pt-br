---
description: A propriedade SourceListInfo do objeto Product Obtém e define as propriedades de informações de origem de um produto. Essa propriedade chama MsiSourceListGetInfo ou MsiSourceListSetInfo. Esta é uma propriedade de leitura ou gravação.
ms.assetid: 3a2c4af5-592f-4acd-b7d8-df163e00b1e2
title: Propriedade Product. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 23fff0cd478a8345e72b79632817e856c40eb7b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748759"
---
# <a name="productsourcelistinfo-property"></a><span data-ttu-id="9e14c-105">Propriedade Product. SourceListInfo</span><span class="sxs-lookup"><span data-stu-id="9e14c-105">Product.SourceListInfo property</span></span>

<span data-ttu-id="9e14c-106">A propriedade **SourceListInfo** do objeto [**Product**](product-object.md) Obtém e define as propriedades de informações de origem de um produto.</span><span class="sxs-lookup"><span data-stu-id="9e14c-106">The **SourceListInfo** property of the [**Product**](product-object.md) object gets and sets the source information properties for a product.</span></span> <span data-ttu-id="9e14c-107">Essa propriedade chama [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="9e14c-107">This property calls [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="9e14c-108">Esta é uma propriedade de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="9e14c-108">This is a read or write property.</span></span>

<span data-ttu-id="9e14c-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="9e14c-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e14c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e14c-110">Syntax</span></span>


```JScript
propVal = Product.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="9e14c-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="9e14c-111">Property value</span></span>

<span data-ttu-id="9e14c-112">O nome das propriedades de informações de origem de um produto a ser consultado ou definido.</span><span class="sxs-lookup"><span data-stu-id="9e14c-112">The name of the source information properties for a product to query or set.</span></span> <span data-ttu-id="9e14c-113">Para obter os valores possíveis, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="9e14c-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e14c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e14c-114">Remarks</span></span>

<span data-ttu-id="9e14c-115">Nem todas as propriedades que podem ser recuperadas podem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="9e14c-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="9e14c-116">O parâmetro *szProperty* pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9e14c-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="9e14c-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9e14c-117">Property</span></span>         | <span data-ttu-id="9e14c-118">Pode definir?</span><span class="sxs-lookup"><span data-stu-id="9e14c-118">Can set?</span></span> | <span data-ttu-id="9e14c-119">Significado</span><span class="sxs-lookup"><span data-stu-id="9e14c-119">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e14c-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="9e14c-120">MediaPackagePath</span></span> | <span data-ttu-id="9e14c-121">S</span><span class="sxs-lookup"><span data-stu-id="9e14c-121">Y</span></span>        | <span data-ttu-id="9e14c-122">O caminho relativo à raiz da mídia de instalação.</span><span class="sxs-lookup"><span data-stu-id="9e14c-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="9e14c-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="9e14c-123">DiskPrompt</span></span>       | <span data-ttu-id="9e14c-124">S</span><span class="sxs-lookup"><span data-stu-id="9e14c-124">Y</span></span>        | <span data-ttu-id="9e14c-125">O modelo de prompt usado ao solicitar a mídia de instalação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9e14c-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="9e14c-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="9e14c-126">LastUsedSource</span></span>   | <span data-ttu-id="9e14c-127">S</span><span class="sxs-lookup"><span data-stu-id="9e14c-127">Y</span></span>        | <span data-ttu-id="9e14c-128">O local de origem usado mais recentemente para o produto.</span><span class="sxs-lookup"><span data-stu-id="9e14c-128">The most recently used source location for the product.</span></span> <span data-ttu-id="9e14c-129">Quando você define essa propriedade, Prefixe o local de origem com "n;" para uma fonte de rede ou "u;" para o tipo de URL.</span><span class="sxs-lookup"><span data-stu-id="9e14c-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="9e14c-130">Por exemplo, "n; \\ \\ Rabisco \\ \\ MySource "e" u; https://MyServer/MyFolder/MySource ".</span><span class="sxs-lookup"><span data-stu-id="9e14c-130">For example, "n;\\\\scratch\\scratch\\MySource" and "u;https://MyServer/MyFolder/MySource".</span></span> |
| <span data-ttu-id="9e14c-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="9e14c-131">LastUsedType</span></span>     | <span data-ttu-id="9e14c-132">N</span><span class="sxs-lookup"><span data-stu-id="9e14c-132">N</span></span>        | <span data-ttu-id="9e14c-133">"n" se a fonte do último usado for um local de rede.</span><span class="sxs-lookup"><span data-stu-id="9e14c-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="9e14c-134">"u" se a última origem usada era um local de URL.</span><span class="sxs-lookup"><span data-stu-id="9e14c-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="9e14c-135">"m" se a última origem usada era a mídia.</span><span class="sxs-lookup"><span data-stu-id="9e14c-135">"m" if the last used source was media.</span></span> <span data-ttu-id="9e14c-136">Cadeia de caracteres vazia ("") se não houver uma última fonte usada.</span><span class="sxs-lookup"><span data-stu-id="9e14c-136">Empty string ("") if there is no last used source.</span></span>                                                                   |
| <span data-ttu-id="9e14c-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="9e14c-137">PackageName</span></span>      | <span data-ttu-id="9e14c-138">S</span><span class="sxs-lookup"><span data-stu-id="9e14c-138">Y</span></span>        | <span data-ttu-id="9e14c-139">O nome do pacote de Windows Installer ou pacote de patch na origem.</span><span class="sxs-lookup"><span data-stu-id="9e14c-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="9e14c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e14c-140">Requirements</span></span>



| <span data-ttu-id="9e14c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e14c-141">Requirement</span></span> | <span data-ttu-id="9e14c-142">Valor</span><span class="sxs-lookup"><span data-stu-id="9e14c-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e14c-143">Versão</span><span class="sxs-lookup"><span data-stu-id="9e14c-143">Version</span></span><br/> | <span data-ttu-id="9e14c-144">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9e14c-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9e14c-145">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e14c-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9e14c-146">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9e14c-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9e14c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9e14c-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="9e14c-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e14c-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9e14c-149">IID</span><span class="sxs-lookup"><span data-stu-id="9e14c-149">IID</span></span><br/>     | <span data-ttu-id="9e14c-150">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9e14c-150">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="9e14c-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e14c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e14c-152">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="9e14c-152">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="9e14c-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9e14c-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="9e14c-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="9e14c-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="9e14c-155">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="9e14c-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




