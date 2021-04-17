---
title: Elemento Image (SDK do WMP)
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento Image (SDK do WMP)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Elemento Image do Windows Media Player
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779996"
---
# <a name="image-element-wmp-sdk"></a><span data-ttu-id="6e24c-105">Elemento Image (SDK do WMP)</span><span class="sxs-lookup"><span data-stu-id="6e24c-105">Image Element (WMP SDK)</span></span>

> [!Note]  
> <span data-ttu-id="6e24c-106">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="6e24c-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6e24c-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="6e24c-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6e24c-108">O elemento **Image** especifica as imagens que o Windows Media Player exibe para o usuário para representar a loja online.</span><span class="sxs-lookup"><span data-stu-id="6e24c-108">The **Image** element specifies the images that Windows Media Player displays to the user to represent the online store.</span></span>

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="6e24c-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="6e24c-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="6e24c-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (necessário para armazenamentos do tipo 1, ignorado para o tipo 2)</span><span class="sxs-lookup"><span data-stu-id="6e24c-110"><span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (required for type 1 stores, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="6e24c-111">URL do logotipo que o Windows Media Player exibe na caixa de diálogo EULA (contrato de licença de usuário final).</span><span class="sxs-lookup"><span data-stu-id="6e24c-111">URL for the logo that Windows Media Player displays in the end user license agreement (EULA) dialog box.</span></span> <span data-ttu-id="6e24c-112">Deve ser uma imagem PNG que seja 80 x 80 pixels.</span><span class="sxs-lookup"><span data-stu-id="6e24c-112">This must be a PNG image that is 80 x 80 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6e24c-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (opcional)</span><span class="sxs-lookup"><span data-stu-id="6e24c-113"><span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="6e24c-114">URL da imagem que o Windows Media Player exibe no menu serviços.</span><span class="sxs-lookup"><span data-stu-id="6e24c-114">URL for the image that Windows Media Player displays on the services menu.</span></span> <span data-ttu-id="6e24c-115">Essa imagem deve ter 15 x 15 pixels.</span><span class="sxs-lookup"><span data-stu-id="6e24c-115">This image must be 15 x 15 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6e24c-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (opcional)</span><span class="sxs-lookup"><span data-stu-id="6e24c-116"><span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="6e24c-117">Para um repositório online tipo 1, essa é a URL para a imagem que o Windows Media Player exibe na guia **lojas online** . Para o Windows Media Player 11, essa imagem deve ter 45 pixels de largura por 13 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="6e24c-117">For a type 1 online store, this is the URL for the image that Windows Media Player displays on the **Online Stores** tab. For Windows Media Player 11, this image must be 45 pixels wide by 13 pixels high.</span></span> <span data-ttu-id="6e24c-118">Para o Windows Media Player 12, essa imagem deve ter 45 pixels de largura por 30 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="6e24c-118">For Windows Media Player 12, this image must be 45 pixels wide by 30 pixels high.</span></span> <span data-ttu-id="6e24c-119">Para dar suporte a ambas as versões 11 e 12 do Windows Media Player, você deve fornecer dois documentos ServiceInfo.xml separados, cada um apontando para a imagem de tamanho adequado para ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="6e24c-119">To support both versions 11 and 12 of Windows Media Player, you must provide two separate ServiceInfo.xml documents, each of which points to the appropriately sized image for ServiceLargeURL.</span></span>

<span data-ttu-id="6e24c-120">Para uma loja online tipo 2, essa é a URL da imagem que o Windows Media Player exibe ao lado da guia **lojas online** ou ao lado dos botões do painel de tarefas.</span><span class="sxs-lookup"><span data-stu-id="6e24c-120">For a type 2 online store, this is the URL for the image that Windows Media Player displays beside the **Online Stores** tab or beside the task pane buttons.</span></span> <span data-ttu-id="6e24c-121">Essa imagem deve ter 30 x 30 pixels.</span><span class="sxs-lookup"><span data-stu-id="6e24c-121">This image must be 30 x 30 pixels.</span></span>

</dd> <dt>

<span data-ttu-id="6e24c-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (opcional)</span><span class="sxs-lookup"><span data-stu-id="6e24c-122"><span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="6e24c-123">URL do logotipo que é exibido junto com a descrição de marketing especificada no elemento **Description** .</span><span class="sxs-lookup"><span data-stu-id="6e24c-123">URL for the logo that is displayed along with the marketing description specified in the **Description** element.</span></span> <span data-ttu-id="6e24c-124">Se não for fornecido, ele ficará em branco.</span><span class="sxs-lookup"><span data-stu-id="6e24c-124">If it is not supplied, it will be blank.</span></span> <span data-ttu-id="6e24c-125">(Todos os tipos, opcional) Essa deve ser uma imagem PNG com 45 pixels de largura e 13 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="6e24c-125">(All types, optional) This must be a PNG image that is 45 pixels wide and 13 pixels high.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="6e24c-126">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="6e24c-126">Parent/Child Elements</span></span>



| <span data-ttu-id="6e24c-127">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="6e24c-127">Hierarchy</span></span>       | <span data-ttu-id="6e24c-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="6e24c-128">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="6e24c-129">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6e24c-129">Parent elements</span></span> | <span data-ttu-id="6e24c-130">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="6e24c-130">**ServiceInfo**</span></span> |
| <span data-ttu-id="6e24c-131">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6e24c-131">Child elements</span></span>  | <span data-ttu-id="6e24c-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6e24c-132">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="6e24c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e24c-133">Remarks</span></span>

<span data-ttu-id="6e24c-134">Os formatos de imagem com suporte são. gif,. jpg,. bmp e. png (que é o formato recomendado).</span><span class="sxs-lookup"><span data-stu-id="6e24c-134">The supported image formats are .gif, .jpg, .bmp, and .png (which is the recommended format).</span></span> <span data-ttu-id="6e24c-135">O uso de transparência da Web tem suporte e é recomendado.</span><span class="sxs-lookup"><span data-stu-id="6e24c-135">Using Web transparency is both supported and recommended.</span></span> <span data-ttu-id="6e24c-136">Não há suporte para arquivos GIF animados.</span><span class="sxs-lookup"><span data-stu-id="6e24c-136">Animated GIF files are not supported.</span></span>

<span data-ttu-id="6e24c-137">Se você não fornecer um valor para **MenuURL**, o Windows Media Player não exibirá nenhum gráfico no menu para sua loja online.</span><span class="sxs-lookup"><span data-stu-id="6e24c-137">If you do not supply a value for **MenuURL**, Windows Media Player displays no graphic on the menu for your online store.</span></span>

<span data-ttu-id="6e24c-138">Você pode fornecer uma imagem animada para ServiceLargeURL.</span><span class="sxs-lookup"><span data-stu-id="6e24c-138">You can provide an animated image for ServiceLargeURL.</span></span> <span data-ttu-id="6e24c-139">No Windows Media Player 10 ou 11, a imagem é animada.</span><span class="sxs-lookup"><span data-stu-id="6e24c-139">In Windows Media Player 10 or 11, the image is animated.</span></span> <span data-ttu-id="6e24c-140">No Windows Media Player 12, somente o primeiro quadro da imagem é exibido.</span><span class="sxs-lookup"><span data-stu-id="6e24c-140">In Windows Media Player 12, only the first frame of the image is displayed.</span></span> <span data-ttu-id="6e24c-141">Para fornecer uma imagem animada, crie um único arquivo de imagem que contenha quadros sucessivos de sua animação.</span><span class="sxs-lookup"><span data-stu-id="6e24c-141">To provide an animated image, create a single image file that contains successive frames of your animation.</span></span> <span data-ttu-id="6e24c-142">Por exemplo, para uma imagem com 30 pixels de largura e 30 pixels de altura, você pode fornecer 20 imagens sucessivas lado a lado em uma imagem com 600 pixels de largura e 30 pixels de altura.</span><span class="sxs-lookup"><span data-stu-id="6e24c-142">For example, for an image that is 30 pixels wide and 30 pixels high, you could supply 20 successive images side by side in an image that is 600 pixels wide and 30 pixels high.</span></span> <span data-ttu-id="6e24c-143">O Windows Media Player animaria essa imagem automaticamente mostrando as 20 imagens individuais uma após a outra.</span><span class="sxs-lookup"><span data-stu-id="6e24c-143">Windows Media Player would automatically animate such an image by showing the 20 individual images one after another.</span></span> <span data-ttu-id="6e24c-144">Essa animação ocorre apenas uma vez quando a loja online é aberta; Ele não se repete.</span><span class="sxs-lookup"><span data-stu-id="6e24c-144">This animation occurs only once when the online store opens; it does not repeat.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e24c-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e24c-145">Requirements</span></span>



| <span data-ttu-id="6e24c-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e24c-146">Requirement</span></span> | <span data-ttu-id="6e24c-147">Valor</span><span class="sxs-lookup"><span data-stu-id="6e24c-147">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="6e24c-148">Versão</span><span class="sxs-lookup"><span data-stu-id="6e24c-148">Version</span></span><br/> | <span data-ttu-id="6e24c-149">Windows Media Player 10 ou posterior</span><span class="sxs-lookup"><span data-stu-id="6e24c-149">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6e24c-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e24c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e24c-151">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="6e24c-151">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="6e24c-152">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="6e24c-152">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="6e24c-153">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="6e24c-153">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





