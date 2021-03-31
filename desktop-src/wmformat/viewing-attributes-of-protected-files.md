---
title: Exibindo atributos de arquivos protegidos
description: Exibindo atributos de arquivos protegidos
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- SDK do Windows Media Format, exibindo atributos de arquivos protegidos
- SDK do Windows Media Format, atributos de arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
- ASF (Advanced Systems Format), exibindo atributos de arquivos protegidos
- ASF (formato de sistemas avançados), exibindo atributos de arquivos protegidos
- ASF (Advanced Systems Format), atributos de arquivos protegidos
- ASF (formato de sistemas avançados), atributos de arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- DRM (gerenciamento de direitos digitais), exibindo atributos de arquivos protegidos
- DRM (gerenciamento de direitos digitais), exibindo atributos de arquivos protegidos
- DRM (gerenciamento de direitos digitais), atributos de arquivos protegidos
- DRM (gerenciamento de direitos digitais), atributos de arquivos protegidos
- DRM (gerenciamento de direitos digitais), arquivos protegidos
- DRM (gerenciamento de direitos digitais), arquivos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640120"
---
# <a name="viewing-attributes-of-protected-files"></a><span data-ttu-id="5ce2a-118">Exibindo atributos de arquivos protegidos</span><span class="sxs-lookup"><span data-stu-id="5ce2a-118">Viewing Attributes of Protected Files</span></span>

<span data-ttu-id="5ce2a-119">Em alguns cenários, talvez seja necessário recuperar determinados atributos DRM em um arquivo sem realmente acessar o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-119">In some scenarios, you may need to retrieve certain DRM attributes in a file without actually accessing the contents of the file.</span></span> <span data-ttu-id="5ce2a-120">Esse recurso é útil, por exemplo, em aplicativos que processam lotes de arquivos de maneiras diferentes com base nas informações no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-120">This capability is useful, for example, in applications that process batches of files in different ways based on information in the file header.</span></span> <span data-ttu-id="5ce2a-121">Nas versões anteriores do Windows Media Format SDK, eram necessários aplicativos para vincular à biblioteca estática do DRM a fim de abrir qualquer arquivo protegido.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-121">In previous versions of the Windows Media Format SDK, applications were required to link to the DRM static library in order to open any protected file.</span></span> <span data-ttu-id="5ce2a-122">Os aplicativos que não têm a biblioteca DRM podem usar a interface [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) no objeto editor de metadados para examinar determinados atributos DRM.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-122">Applications that do not have the DRM library can use the [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) interface on the metadata editor object to examine certain DRM attributes.</span></span>

> [!Note]  
> <span data-ttu-id="5ce2a-123">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="5ce2a-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5ce2a-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ce2a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ce2a-125">**Lista de atributos DRM**</span><span class="sxs-lookup"><span data-stu-id="5ce2a-125">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="5ce2a-126">**Habilitando o suporte a DRM**</span><span class="sxs-lookup"><span data-stu-id="5ce2a-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="5ce2a-127">**Interface IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="5ce2a-127">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




