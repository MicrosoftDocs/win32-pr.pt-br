---
title: Metadados personalizados
description: Metadados personalizados
ms.assetid: 86132163-da56-416a-9539-874d18972932
keywords:
- SDK do Windows Media Format, metadados personalizados
- ASF (Advanced Systems Format), metadados personalizados
- ASF (formato de sistemas avançados), metadados personalizados
- SDK do Windows Media Format, interface IWMHeaderInfo3
- Formato de sistema avançado (ASF), interface IWMHeaderInfo3
- ASF (formato de sistemas avançados), interface IWMHeaderInfo3
- metadados, personalizando
- IWMHeaderInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a795ab184e5bd6120278f61c0d3654679fd79c28
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103640280"
---
# <a name="custom-metadata"></a><span data-ttu-id="e6529-111">Metadados personalizados</span><span class="sxs-lookup"><span data-stu-id="e6529-111">Custom Metadata</span></span>

<span data-ttu-id="e6529-112">Além dos muitos atributos com suporte fornecidos com o Windows Media Format SDK, você pode criar atributos de metadados para suas próprias especificações.</span><span class="sxs-lookup"><span data-stu-id="e6529-112">In addition to the many supported attributes provided with the Windows Media Format SDK, you can create metadata attributes to your own specifications.</span></span> <span data-ttu-id="e6529-113">Ao criar atributos de metadados personalizados, você deve usar uma Convenção de nomenclatura facilmente identificável para evitar possíveis conflitos com atributos criados por outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="e6529-113">When creating custom metadata attributes, you should use an easily identifiable naming convention to avoid possible conflict with attributes created by others.</span></span>

<span data-ttu-id="e6529-114">É recomendável que você use os métodos de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) para criar seus metadados devido à flexibilidade adicional que eles fornecem sobre os métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span><span class="sxs-lookup"><span data-stu-id="e6529-114">It is recommended that you use the methods of [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) to create your metadata because of the added flexibility they provide over the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6529-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e6529-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6529-116">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="e6529-116">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="e6529-117">**Recursos de metadados**</span><span class="sxs-lookup"><span data-stu-id="e6529-117">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="e6529-118">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="e6529-118">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




