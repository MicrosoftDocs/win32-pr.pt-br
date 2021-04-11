---
title: Exibindo atributos DRM no editor de metadados
description: Exibindo atributos DRM no editor de metadados
ms.assetid: e25fb8c8-8f4d-40fd-aa6f-675921e0ccdd
keywords:
- SDK do Windows Media Format, exibição de atributo DRM
- DRM (gerenciamento de direitos digitais), exibição de atributo
- DRM (gerenciamento de direitos digitais), exibição de atributo
- SDK do Windows Media Format, editor de metadados
- DRM (gerenciamento de direitos digitais), editor de metadados
- DRM (gerenciamento de direitos digitais), editor de metadados
- SDK do Windows Media Format, interface IWMDRMEditor
- DRM (gerenciamento de direitos digitais), interface IWMDRMEditor
- DRM (gerenciamento de direitos digitais), interface IWMDRMEditor
- Editor de metadados, exibição de atributo DRM
- Editor de metadados, interface IWMDRMEditor
- IWMDRMEditor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8541444ad7704ecc340476929f1205f11ccd61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293786"
---
# <a name="viewing-drm-attributes-in-the-metadata-editor"></a><span data-ttu-id="7693a-115">Exibindo atributos DRM no editor de metadados</span><span class="sxs-lookup"><span data-stu-id="7693a-115">Viewing DRM Attributes in the Metadata Editor</span></span>

<span data-ttu-id="7693a-116">O editor de metadados expõe a interface IWMDRMEditor, que permite a edição de aplicativos para examinar determinados atributos de um cabeçalho DRM em um arquivo ASF protegido, e os atributos na licença de conteúdo, se houver, mesmo que o aplicativo não tenha a biblioteca estática específica do DRM (wmstubdrm. lib) que seja necessária para aplicativos do DRM Player e do gravador totalmente habilitados.</span><span class="sxs-lookup"><span data-stu-id="7693a-116">The Metadata Editor exposes the IWMDRMEditor interface, which enables editing applications to examine certain attributes of a DRM header in a protected ASF file, and attributes in the content license, if one is present, even if the application doesn't have the DRM-specific static library (wmstubdrm.lib) that is required for fully-enabled DRM player and writer applications.</span></span>

> [!Note]  
> <span data-ttu-id="7693a-117">O DRM não é compatível com a versão baseada em x64 deste SDK.</span><span class="sxs-lookup"><span data-stu-id="7693a-117">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7693a-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7693a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7693a-119">**Recursos de Rights Management digital**</span><span class="sxs-lookup"><span data-stu-id="7693a-119">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="7693a-120">**Interface IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="7693a-120">**IWMDRMEditor Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




