---
title: Definindo atributos de metadados
description: Definindo atributos de metadados
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- SDK do Windows Media Format, definindo atributos de metadados
- ASF (Advanced Systems Format), definindo atributos de metadados
- ASF (formato de sistemas avançados), definindo atributos de metadados
- metadados, definindo atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfde27d7bc965076d1a4b5f9674c6d198ce61da5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365605"
---
# <a name="setting-metadata-attributes"></a><span data-ttu-id="4a897-107">Definindo atributos de metadados</span><span class="sxs-lookup"><span data-stu-id="4a897-107">Setting Metadata Attributes</span></span>

<span data-ttu-id="4a897-108">Os atributos de metadados são definidos usando o método [**IWMHeaderInfo3:: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .</span><span class="sxs-lookup"><span data-stu-id="4a897-108">Metadata attributes are set by using the [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) method.</span></span>

<span data-ttu-id="4a897-109">Todos os atributos são atribuídos a um idioma da lista de idiomas para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="4a897-109">All attributes are assigned a language from the language list for the file.</span></span> <span data-ttu-id="4a897-110">Você pode acessar a lista de idiomas usando a interface [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) .</span><span class="sxs-lookup"><span data-stu-id="4a897-110">You can access the language list by using the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface.</span></span> <span data-ttu-id="4a897-111">Para obter um ponteiro para uma interface **IWMLanguageList** , chame **QueryInterface** em qualquer interface do objeto do qual você obteve [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span><span class="sxs-lookup"><span data-stu-id="4a897-111">To get a pointer to an **IWMLanguageList** interface, call **QueryInterface** on any interface of the object from which you have obtained [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).</span></span>

<span data-ttu-id="4a897-112">Você pode adicionar atributos com qualquer nome que desejar.</span><span class="sxs-lookup"><span data-stu-id="4a897-112">You can add attributes with any name you like.</span></span> <span data-ttu-id="4a897-113">No entanto, o uso de nomes de atributos que não são nomes padrão com suporte pelo Windows Media Format SDK pode dificultar a descoberta dos seus metadados.</span><span class="sxs-lookup"><span data-stu-id="4a897-113">However, using attribute names that are not standard names supported by the Windows Media Format SDK can make your metadata difficult for users to discover.</span></span> <span data-ttu-id="4a897-114">A maioria dos aplicativos de reprodução de mídia verificará se há valores padrão.</span><span class="sxs-lookup"><span data-stu-id="4a897-114">Most media-playing applications will check for standard values.</span></span> <span data-ttu-id="4a897-115">Para obter mais informações, consulte [metadados personalizados](custom-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="4a897-115">For more information, see [Custom Metadata](custom-metadata.md).</span></span>

<span data-ttu-id="4a897-116">Você não pode usar o número de fluxo 0xFFFF para adicionar um atributo globalmente.</span><span class="sxs-lookup"><span data-stu-id="4a897-116">You cannot use stream number 0xFFFF to add an attribute globally.</span></span> <span data-ttu-id="4a897-117">Você deve atribuir cada atributo a um número de fluxo específico ou o fluxo 0 para atributos de nível de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4a897-117">You must assign each attribute to a specific stream number, or stream 0 for file-level attributes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a897-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a897-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a897-119">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="4a897-119">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




