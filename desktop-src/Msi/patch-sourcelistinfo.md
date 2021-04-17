---
description: A propriedade SourceListInfo do objeto patch Obtém e define as propriedades de informações de origem para um patch. Esta propriedade chama MsiSourceListGetInfo ou MsiSourceListSetInfo. Esta é uma propriedade de leitura ou gravação.
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: Propriedade patch. SourceListInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22f4428decca7629f9d4049a2d3f52dfe8b8775a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747747"
---
# <a name="patchsourcelistinfo-property"></a><span data-ttu-id="a242d-105">Propriedade patch. SourceListInfo</span><span class="sxs-lookup"><span data-stu-id="a242d-105">Patch.SourceListInfo property</span></span>

<span data-ttu-id="a242d-106">A propriedade **SourceListInfo** do objeto [**patch**](patch-object.md) Obtém e define as propriedades de informações de origem para um patch.</span><span class="sxs-lookup"><span data-stu-id="a242d-106">The **SourceListInfo** property of the [**Patch**](patch-object.md) object gets and sets the source information properties for a patch.</span></span> <span data-ttu-id="a242d-107">Esta propriedade chama [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) ou [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span><span class="sxs-lookup"><span data-stu-id="a242d-107">This property call [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) or [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa).</span></span> <span data-ttu-id="a242d-108">Esta é uma propriedade de leitura ou gravação.</span><span class="sxs-lookup"><span data-stu-id="a242d-108">This is a read or write property.</span></span>

<span data-ttu-id="a242d-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a242d-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a242d-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a242d-110">Syntax</span></span>


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a><span data-ttu-id="a242d-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a242d-111">Property value</span></span>

<span data-ttu-id="a242d-112">O nome das propriedades de informações de origem para um patch a ser consultado ou definido.</span><span class="sxs-lookup"><span data-stu-id="a242d-112">The name of the source information properties for a patch to query or set.</span></span> <span data-ttu-id="a242d-113">Para obter os valores possíveis, consulte a seção comentários deste tópico.</span><span class="sxs-lookup"><span data-stu-id="a242d-113">For possible values, see the Remarks section of this topic.</span></span>

## <a name="remarks"></a><span data-ttu-id="a242d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a242d-114">Remarks</span></span>

<span data-ttu-id="a242d-115">Nem todas as propriedades que podem ser recuperadas podem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="a242d-115">Not all properties that can be retrieved can be set.</span></span> <span data-ttu-id="a242d-116">O parâmetro *szProperty* pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a242d-116">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="a242d-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a242d-117">Property</span></span>         | <span data-ttu-id="a242d-118">Pode definir?</span><span class="sxs-lookup"><span data-stu-id="a242d-118">Can set?</span></span> | <span data-ttu-id="a242d-119">Significado</span><span class="sxs-lookup"><span data-stu-id="a242d-119">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a242d-120">MediaPackagePath</span><span class="sxs-lookup"><span data-stu-id="a242d-120">MediaPackagePath</span></span> | <span data-ttu-id="a242d-121">S</span><span class="sxs-lookup"><span data-stu-id="a242d-121">Y</span></span>        | <span data-ttu-id="a242d-122">O caminho relativo à raiz da mídia de instalação.</span><span class="sxs-lookup"><span data-stu-id="a242d-122">The path relative to the root of the installation media.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="a242d-123">DiskPrompt</span><span class="sxs-lookup"><span data-stu-id="a242d-123">DiskPrompt</span></span>       | <span data-ttu-id="a242d-124">S</span><span class="sxs-lookup"><span data-stu-id="a242d-124">Y</span></span>        | <span data-ttu-id="a242d-125">O modelo de prompt usado ao solicitar a mídia de instalação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a242d-125">The prompt template used when prompting the user for installation media.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="a242d-126">LastUsedSource</span><span class="sxs-lookup"><span data-stu-id="a242d-126">LastUsedSource</span></span>   | <span data-ttu-id="a242d-127">S</span><span class="sxs-lookup"><span data-stu-id="a242d-127">Y</span></span>        | <span data-ttu-id="a242d-128">O local de origem usado mais recentemente para o patch.</span><span class="sxs-lookup"><span data-stu-id="a242d-128">The most recently used source location for the patch.</span></span> <span data-ttu-id="a242d-129">Quando você define essa propriedade, Prefixe o local de origem com "n;" para uma fonte de rede ou "u;" para o tipo de URL.</span><span class="sxs-lookup"><span data-stu-id="a242d-129">When you set this property, prefix the source location with "n;" for a network source or "u;" for URL type.</span></span> <span data-ttu-id="a242d-130">Por exemplo, use "n; \\ \\ \\ \\ teste de rascunho transitório "ou" u; https://microsoft.com/Patches/Office/SP1 ".</span><span class="sxs-lookup"><span data-stu-id="a242d-130">For example, use "n;\\\\scratch\\scratch\\test" or "u;https://microsoft.com/Patches/Office/SP1".</span></span> |
| <span data-ttu-id="a242d-131">LastUsedType</span><span class="sxs-lookup"><span data-stu-id="a242d-131">LastUsedType</span></span>     | <span data-ttu-id="a242d-132">N</span><span class="sxs-lookup"><span data-stu-id="a242d-132">N</span></span>        | <span data-ttu-id="a242d-133">"n" se a fonte do último usado for um local de rede.</span><span class="sxs-lookup"><span data-stu-id="a242d-133">"n" if the last-used source is a network location.</span></span> <span data-ttu-id="a242d-134">"u" se a última origem usada era um local de URL.</span><span class="sxs-lookup"><span data-stu-id="a242d-134">"u" if the last used source was a URL location.</span></span> <span data-ttu-id="a242d-135">"m" se a última origem usada era a mídia.</span><span class="sxs-lookup"><span data-stu-id="a242d-135">"m" if the last used source was media.</span></span> <span data-ttu-id="a242d-136">Cadeia de caracteres vazia ("") se não houver uma última fonte usada.</span><span class="sxs-lookup"><span data-stu-id="a242d-136">Empty string ("") if there is no last used source.</span></span>                                                                      |
| <span data-ttu-id="a242d-137">PackageName</span><span class="sxs-lookup"><span data-stu-id="a242d-137">PackageName</span></span>      | <span data-ttu-id="a242d-138">S</span><span class="sxs-lookup"><span data-stu-id="a242d-138">Y</span></span>        | <span data-ttu-id="a242d-139">O nome do pacote de Windows Installer ou pacote de patch na origem.</span><span class="sxs-lookup"><span data-stu-id="a242d-139">The name of the Windows Installer package or patch package on the source.</span></span>                                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="a242d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a242d-140">Requirements</span></span>



| <span data-ttu-id="a242d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a242d-141">Requirement</span></span> | <span data-ttu-id="a242d-142">Valor</span><span class="sxs-lookup"><span data-stu-id="a242d-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a242d-143">Versão</span><span class="sxs-lookup"><span data-stu-id="a242d-143">Version</span></span><br/> | <span data-ttu-id="a242d-144">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a242d-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a242d-145">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a242d-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a242d-146">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a242d-146">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a242d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a242d-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="a242d-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a242d-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a242d-149">IID</span><span class="sxs-lookup"><span data-stu-id="a242d-149">IID</span></span><br/>     | <span data-ttu-id="a242d-150">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a242d-150">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a242d-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="a242d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a242d-152">**Patch**</span><span class="sxs-lookup"><span data-stu-id="a242d-152">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="a242d-153">**MsiSourceListGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a242d-153">**MsiSourceListGetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[<span data-ttu-id="a242d-154">**MsiSourceListSetInfo**</span><span class="sxs-lookup"><span data-stu-id="a242d-154">**MsiSourceListSetInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[<span data-ttu-id="a242d-155">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="a242d-155">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




