---
description: O Windows Vista faz mais uso de imagens em miniaturas específicas de arquivo do que as versões anteriores do Windows.
title: Manipuladores de miniatura
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171173"
---
# <a name="thumbnail-handlers"></a><span data-ttu-id="1124c-103">Manipuladores de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-103">Thumbnail Handlers</span></span>

<span data-ttu-id="1124c-104">O Windows Vista faz mais uso de imagens em miniaturas específicas de arquivo do que as versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="1124c-104">Windows Vista makes greater use of file-specific thumbnail images than earlier versions of Windows.</span></span> <span data-ttu-id="1124c-105">O Windows Vista os usa em todas as exibições, em caixas de diálogo e em qualquer tipo de arquivo que as forneça.</span><span class="sxs-lookup"><span data-stu-id="1124c-105">Windows Vista uses them in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="1124c-106">Outros aplicativos também podem consumir sua miniatura.</span><span class="sxs-lookup"><span data-stu-id="1124c-106">Other applications can consume your thumbnail as well.</span></span> <span data-ttu-id="1124c-107">A exibição de miniatura também foi alterada.</span><span class="sxs-lookup"><span data-stu-id="1124c-107">Thumbnail display has also changed.</span></span> <span data-ttu-id="1124c-108">Agora, um espectro contínuo de tamanhos selecionáveis pelo usuário está disponível em vez de tamanhos discretos, como ícones e miniaturas fornecidos no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1124c-108">Now, a continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails provided in Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="1124c-109">Você pode ouvir essas miniaturas conhecidas como ícones dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="1124c-109">You might hear these thumbnails referred to as Live Icons.</span></span>

 

<span data-ttu-id="1124c-110">As miniaturas de resolução de 32 bits e tão grandes quanto 256x256 pixels geralmente são usadas na interface do usuário do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1124c-110">Thumbnails of 32-bit resolution and as large as 256x256 pixels are often used in Windows Vista UI.</span></span> <span data-ttu-id="1124c-111">Os proprietários de formato de arquivo devem estar preparados para exibir suas miniaturas nesse tamanho.</span><span class="sxs-lookup"><span data-stu-id="1124c-111">File format owners should be prepared to display their thumbnails at that size.</span></span> <span data-ttu-id="1124c-112">Eles também devem fornecer imagens não estáticas para suas miniaturas que refletem o conteúdo do arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="1124c-112">They should also provide non-static images for their thumbnails that reflect the particular file's contents.</span></span> <span data-ttu-id="1124c-113">Por exemplo, a miniatura de um arquivo de texto deve mostrar uma versão em miniatura do documento, incluindo seu texto.</span><span class="sxs-lookup"><span data-stu-id="1124c-113">For example, a text file's thumbnail should show a miniature version of the document, including its text.</span></span>

<span data-ttu-id="1124c-114">A interface [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) foi introduzida para tornar o fornecimento de uma miniatura mais fácil e mais simples do que no passado, quando [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) teria sido usado em vez disso.</span><span class="sxs-lookup"><span data-stu-id="1124c-114">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface has been introduced to make providing a thumbnail easier and more straightforward than in the past, when [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) would have been used instead.</span></span> <span data-ttu-id="1124c-115">Observe que o código existente que usa **IExtractImage** ainda é válido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1124c-115">Note, that existing code that uses **IExtractImage** is still valid under Windows Vista.</span></span> <span data-ttu-id="1124c-116">No entanto, não há suporte para **IExtractImage** no painel de **detalhes** .</span><span class="sxs-lookup"><span data-stu-id="1124c-116">However, **IExtractImage** is not supported in the **Details** pane.</span></span>

<span data-ttu-id="1124c-117">Este tópico aborda o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1124c-117">This topic discusses the following:</span></span>

-   [<span data-ttu-id="1124c-118">Processos de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-118">Thumbnail Processes</span></span>](#thumbnail-processes)
-   [<span data-ttu-id="1124c-119">Cache e dimensionamento de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-119">Thumbnail Cache and Sizing</span></span>](#thumbnail-cache-and-sizing)
-   [<span data-ttu-id="1124c-120">Sobreposições de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-120">Thumbnail Overlays</span></span>](#thumbnail-overlays)
-   [<span data-ttu-id="1124c-121">Adornos de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-121">Thumbnail Adornments</span></span>](#thumbnail-adornments)
-   [<span data-ttu-id="1124c-122">Registrando seu manipulador de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1124c-122">Registering Your Thumbnail Handler</span></span>](#registering-your-thumbnail-handler)
-   [<span data-ttu-id="1124c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1124c-123">Related topics</span></span>](#related-topics)

## <a name="thumbnail-processes"></a><span data-ttu-id="1124c-124">Processos de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-124">Thumbnail Processes</span></span>

<span data-ttu-id="1124c-125">Manipuladores, incluindo manipuladores de miniatura, são executados por padrão em um processo separado.</span><span class="sxs-lookup"><span data-stu-id="1124c-125">Handlers, including thumbnail handlers, run by default in a separate process.</span></span> <span data-ttu-id="1124c-126">Você pode forçar o manipulador a ser executado em processo passando um valor **nulo** como o contexto de associação em uma chamada para [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) , conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="1124c-126">You can force the handler to run in-process by passing a **NULL** value as the bind context in a call to [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) as shown here:</span></span>


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



<span data-ttu-id="1124c-127">Você também pode recusar a execução fora do processo por padrão definindo a entrada DisableProcessIsolation no registro, conforme mostrado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="1124c-127">You can also opt out of running out of process by default by setting the DisableProcessIsolation entry in the registry as shown in this example.</span></span> <span data-ttu-id="1124c-128">O CLSID (identificador de classe) {E357FCCD-A995-4576-B01F-234630154E96} é o CLSID para implementações de [**manipuladordeminiaturai**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .</span><span class="sxs-lookup"><span data-stu-id="1124c-128">The class identifier (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} is the CLSID for [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) implementations.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a><span data-ttu-id="1124c-129">Cache e dimensionamento de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-129">Thumbnail Cache and Sizing</span></span>

<span data-ttu-id="1124c-130">Quando uma miniatura é necessária, o Windows verifica primeiro o cache de miniaturas da imagem.</span><span class="sxs-lookup"><span data-stu-id="1124c-130">When a thumbnail is needed, Windows first checks the thumbnail cache for the image.</span></span> <span data-ttu-id="1124c-131">O extrator de miniatura será chamado se a imagem não for encontrada no cache.</span><span class="sxs-lookup"><span data-stu-id="1124c-131">The thumbnail extractor is called if the image is not found in the cache.</span></span> <span data-ttu-id="1124c-132">Ele também é chamado quando a hora da última modificação da imagem é posterior àquela da cópia no cache.</span><span class="sxs-lookup"><span data-stu-id="1124c-132">It is also called when the last modified time of the image is later than that of the copy in the cache.</span></span>

<span data-ttu-id="1124c-133">As imagens em miniatura nesse cache são armazenadas em um conjunto de tamanhos discretos.</span><span class="sxs-lookup"><span data-stu-id="1124c-133">The thumbnail images in this cache are stored in a set of discrete sizes.</span></span> <span data-ttu-id="1124c-134">Todos os tamanhos são fornecidos em pixels.</span><span class="sxs-lookup"><span data-stu-id="1124c-134">All sizes are given in pixels.</span></span>

-   <span data-ttu-id="1124c-135">32x32</span><span class="sxs-lookup"><span data-stu-id="1124c-135">32x32</span></span>
-   <span data-ttu-id="1124c-136">96x96</span><span class="sxs-lookup"><span data-stu-id="1124c-136">96x96</span></span>
-   <span data-ttu-id="1124c-137">256x256</span><span class="sxs-lookup"><span data-stu-id="1124c-137">256x256</span></span>
-   <span data-ttu-id="1124c-138">1024x1024</span><span class="sxs-lookup"><span data-stu-id="1124c-138">1024x1024</span></span>

> [!Note]  
> <span data-ttu-id="1124c-139">Esses valores estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="1124c-139">These values are subject to change.</span></span> <span data-ttu-id="1124c-140">O código não deve pressupor que qualquer tamanho específico sempre será usado.</span><span class="sxs-lookup"><span data-stu-id="1124c-140">You code should not assume that any particular size will always be used.</span></span>

 

<span data-ttu-id="1124c-141">Se uma imagem não for quadrada, você não deverá fazê-la por conta própria.</span><span class="sxs-lookup"><span data-stu-id="1124c-141">If an image is not square, you should not pad it yourself.</span></span> <span data-ttu-id="1124c-142">O Windows é responsável por respeitar a taxa de proporção original e preencher a imagem para um tamanho quadrado.</span><span class="sxs-lookup"><span data-stu-id="1124c-142">Windows is responsible for respecting the original aspect ratio and padding the image to a square size.</span></span>

<span data-ttu-id="1124c-143">Quando uma imagem de um determinado tamanho é solicitada, a menos que uma correspondência exata seja encontrada, o Windows Vista sempre recupera a próxima imagem maior e a dimensiona para o tamanho solicitado.</span><span class="sxs-lookup"><span data-stu-id="1124c-143">When an image of a particular size is asked for, unless an exact match is found, Windows Vista always retrieves the next largest image and scales it down to the requested size.</span></span> <span data-ttu-id="1124c-144">Uma imagem nunca é dimensionada em tamanho, como era o caso nas versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="1124c-144">An image is never scaled up in size as was the case in previous versions of Windows.</span></span>

<span data-ttu-id="1124c-145">A tabela a seguir fornece alguns exemplos da relação entre o tamanho solicitado e o tamanho disponível.</span><span class="sxs-lookup"><span data-stu-id="1124c-145">The following table gives some examples of the relationship between requested size and available size.</span></span>



| <span data-ttu-id="1124c-146">Tamanho máximo da imagem que você fornece</span><span class="sxs-lookup"><span data-stu-id="1124c-146">Maximum Image Size You Provide</span></span> | <span data-ttu-id="1124c-147">Tamanho solicitado pelo extrator</span><span class="sxs-lookup"><span data-stu-id="1124c-147">Size Requested by the Extractor</span></span> | <span data-ttu-id="1124c-148">Você fornece</span><span class="sxs-lookup"><span data-stu-id="1124c-148">You Provide</span></span>                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| <span data-ttu-id="1124c-149">156x120</span><span class="sxs-lookup"><span data-stu-id="1124c-149">156x120</span></span>                        | <span data-ttu-id="1124c-150">256x256</span><span class="sxs-lookup"><span data-stu-id="1124c-150">256x256</span></span>                         | <span data-ttu-id="1124c-151">156x120 (não preencha, mantenha a taxa de proporção)</span><span class="sxs-lookup"><span data-stu-id="1124c-151">156x120 (Do not pad, maintain aspect ratio)</span></span> |
| <span data-ttu-id="1124c-152">2048x1024</span><span class="sxs-lookup"><span data-stu-id="1124c-152">2048x1024</span></span>                      | <span data-ttu-id="1124c-153">256x256</span><span class="sxs-lookup"><span data-stu-id="1124c-153">256x256</span></span>                         | <span data-ttu-id="1124c-154">256x128 (não preencha, mantenha a taxa de proporção)</span><span class="sxs-lookup"><span data-stu-id="1124c-154">256x128 (Do not pad, maintain aspect ratio)</span></span> |



 

<span data-ttu-id="1124c-155">Você pode declarar um ponto de corte como parte da entrada de ID do programa do aplicativo associado no registro.</span><span class="sxs-lookup"><span data-stu-id="1124c-155">You can declare a cutoff point as part of the program ID entry of the associated app in the registry.</span></span> <span data-ttu-id="1124c-156">Abaixo desse tamanho, as miniaturas não são usadas.</span><span class="sxs-lookup"><span data-stu-id="1124c-156">Below this size, thumbnails are not used.</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

<span data-ttu-id="1124c-157">A entrada ThumbnailCutoff é um desses valores de REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="1124c-157">The ThumbnailCutoff entry is one of these REG\_DWORD values.</span></span>

| <span data-ttu-id="1124c-158">Valor</span><span class="sxs-lookup"><span data-stu-id="1124c-158">Value</span></span> | <span data-ttu-id="1124c-159">Corte</span><span class="sxs-lookup"><span data-stu-id="1124c-159">Cutoff</span></span> | <span data-ttu-id="1124c-160">HighDPI confidencial</span><span class="sxs-lookup"><span data-stu-id="1124c-160">HighDPI Sensitive</span></span> |
|-------|--------|-------------------|
| <span data-ttu-id="1124c-161">0</span><span class="sxs-lookup"><span data-stu-id="1124c-161">0</span></span>     | <span data-ttu-id="1124c-162">32x32</span><span class="sxs-lookup"><span data-stu-id="1124c-162">32x32</span></span>  | <span data-ttu-id="1124c-163">Sim</span><span class="sxs-lookup"><span data-stu-id="1124c-163">Yes</span></span>               |
| <span data-ttu-id="1124c-164">1</span><span class="sxs-lookup"><span data-stu-id="1124c-164">1</span></span>     | <span data-ttu-id="1124c-165">16x16</span><span class="sxs-lookup"><span data-stu-id="1124c-165">16x16</span></span>  | <span data-ttu-id="1124c-166">Yes</span><span class="sxs-lookup"><span data-stu-id="1124c-166">Yes</span></span>               |
| <span data-ttu-id="1124c-167">2</span><span class="sxs-lookup"><span data-stu-id="1124c-167">2</span></span>     | <span data-ttu-id="1124c-168">48 x 48</span><span class="sxs-lookup"><span data-stu-id="1124c-168">48x48</span></span>  | <span data-ttu-id="1124c-169">Yes</span><span class="sxs-lookup"><span data-stu-id="1124c-169">Yes</span></span>               |
| <span data-ttu-id="1124c-170">3</span><span class="sxs-lookup"><span data-stu-id="1124c-170">3</span></span>     | <span data-ttu-id="1124c-171">16x16</span><span class="sxs-lookup"><span data-stu-id="1124c-171">16x16</span></span>  | <span data-ttu-id="1124c-172">Yes</span><span class="sxs-lookup"><span data-stu-id="1124c-172">Yes</span></span>               |


<span data-ttu-id="1124c-173">A sensibilidade de pontos por polegada (DPI) alta significa que as dimensões de pixel da miniatura se ajustam automaticamente para o dpi maior.</span><span class="sxs-lookup"><span data-stu-id="1124c-173">High dots per inch (dpi) sensitivity means that the pixel dimensions of the thumbnail automatically adjust for the greater dpi.</span></span> <span data-ttu-id="1124c-174">Por exemplo, uma imagem 32x32 em 96 DPI seria uma imagem 40x40 em 120 dpi.</span><span class="sxs-lookup"><span data-stu-id="1124c-174">For instance, a 32x32 image at 96 dpi would be a 40x40 image at 120 dpi.</span></span>

<span data-ttu-id="1124c-175">Se a entrada ThumbnailCutoff não for especificada, o corte padrão será 20x20 (não diferencia DPI).</span><span class="sxs-lookup"><span data-stu-id="1124c-175">If the ThumbnailCutoff entry is not specified, the default cutoff is 20x20 (not dpi-sensitive).</span></span>

## <a name="thumbnail-overlays"></a><span data-ttu-id="1124c-176">Sobreposições de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-176">Thumbnail Overlays</span></span>

<span data-ttu-id="1124c-177">Sobreposições de miniatura, uma imagem pequena exibida no canto inferior direito da miniatura, fornecem uma oportunidade para que os desenvolvedores apliquem identificação de marca às suas miniaturas.</span><span class="sxs-lookup"><span data-stu-id="1124c-177">Thumbnail overlays, a small image displayed over the lower right corner of the thumbnail, provide an opportunity for developers to apply brand identification to their thumbnails.</span></span> <span data-ttu-id="1124c-178">As sobreposições são declaradas no registro como parte da entrada da ID do programa do aplicativo associado, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="1124c-178">Overlays are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

<span data-ttu-id="1124c-179">A entrada TypeOverlay contém um valor de REG \_ sz interpretado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1124c-179">The TypeOverlay entry contains a REG\_SZ value interpreted as follows:</span></span>

-   <span data-ttu-id="1124c-180">Se o valor for uma referência de recurso (um arquivo **. ico** inserido na DLL), como `ISVComponent.dll,-155` , essa imagem será usada como a sobreposição de arquivos com essa extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1124c-180">If the value is a resource reference (a **.ico** file embedded in the DLL) such as `ISVComponent.dll,-155`, that image is used as the overlay for files with that file name extension.</span></span> <span data-ttu-id="1124c-181">Observe que, neste exemplo, **155** é a ID de recurso e, se a dll não estiver presente em um caminho padrão (como **C:/Windows/system32**), o caminho completo será necessário em vez de apenas o nome da dll.</span><span class="sxs-lookup"><span data-stu-id="1124c-181">Note that in this example, **155** is the resouce ID, and if the DLL is not present in a standard path (such as **C:/Windows/System32**), the full path is required instead of just the DLL name.</span></span>
-   <span data-ttu-id="1124c-182">Se o valor for uma cadeia de caracteres vazia, nenhuma sobreposição será aplicada à imagem.</span><span class="sxs-lookup"><span data-stu-id="1124c-182">If the value is an empty string, no overlay is applied to the image.</span></span>
-   <span data-ttu-id="1124c-183">Se o valor não estiver presente, será usado o ícone padrão do aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="1124c-183">If the value is not present, the default icon of the associated application is used.</span></span>

<span data-ttu-id="1124c-184">Sobreposições para suas miniaturas só devem ser fornecidas por meio desse mecanismo e aplicadas pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="1124c-184">Overlays for your thumbnails should only be provided through this mechanism and applied by Windows.</span></span> <span data-ttu-id="1124c-185">Não aplique sobreposições por conta própria.</span><span class="sxs-lookup"><span data-stu-id="1124c-185">Do not apply overlays yourself.</span></span>

## <a name="thumbnail-adornments"></a><span data-ttu-id="1124c-186">Adornos de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-186">Thumbnail Adornments</span></span>

<span data-ttu-id="1124c-187">Adorners como drop Shadows são aplicados a miniaturas com base no tema selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1124c-187">Adornments such as drop shadows are applied to thumbnails based on the user's currently selected theme.</span></span> <span data-ttu-id="1124c-188">Os adornos são fornecidos pelo Windows; Não os crie por conta própria.</span><span class="sxs-lookup"><span data-stu-id="1124c-188">Adornments are provided by Windows; do not create them yourself.</span></span> <span data-ttu-id="1124c-189">O Windows poderia alterar a aparência de adorners específicos a qualquer momento, portanto, se você tiver fornecido a sua conta, correria o risco de ficar fora de sincronia com o sistema.</span><span class="sxs-lookup"><span data-stu-id="1124c-189">Windows could change the look of particular adornments at any time, so if you provided you own you would risk falling out of sync with the system.</span></span> <span data-ttu-id="1124c-190">As miniaturas podem ficar com uma aparência de data ou fora do local.</span><span class="sxs-lookup"><span data-stu-id="1124c-190">Your thumbnails could wind up looking dated or out of place.</span></span>

<span data-ttu-id="1124c-191">Adornos potenciais são declarados no registro como parte da entrada de ID do programa do aplicativo associado, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="1124c-191">Potential adornments are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

<span data-ttu-id="1124c-192">A entrada de tratamento contém um desses valores de REG \_ DWORD:</span><span class="sxs-lookup"><span data-stu-id="1124c-192">The Treatment entry contains one of these REG\_DWORD values:</span></span>



| <span data-ttu-id="1124c-193">Valor</span><span class="sxs-lookup"><span data-stu-id="1124c-193">Value</span></span> | <span data-ttu-id="1124c-194">Significado</span><span class="sxs-lookup"><span data-stu-id="1124c-194">Meaning</span></span>         |
|-------|-----------------|
| <span data-ttu-id="1124c-195">0</span><span class="sxs-lookup"><span data-stu-id="1124c-195">0</span></span>     | <span data-ttu-id="1124c-196">Sem Adornment</span><span class="sxs-lookup"><span data-stu-id="1124c-196">No Adornment</span></span>    |
| <span data-ttu-id="1124c-197">1</span><span class="sxs-lookup"><span data-stu-id="1124c-197">1</span></span>     | <span data-ttu-id="1124c-198">Sombra</span><span class="sxs-lookup"><span data-stu-id="1124c-198">Drop Shadow</span></span>     |
| <span data-ttu-id="1124c-199">2</span><span class="sxs-lookup"><span data-stu-id="1124c-199">2</span></span>     | <span data-ttu-id="1124c-200">Borda da foto</span><span class="sxs-lookup"><span data-stu-id="1124c-200">Photo Border</span></span>    |
| <span data-ttu-id="1124c-201">3</span><span class="sxs-lookup"><span data-stu-id="1124c-201">3</span></span>     | <span data-ttu-id="1124c-202">Sobrerockets de vídeo</span><span class="sxs-lookup"><span data-stu-id="1124c-202">Video Sprockets</span></span> |


<span data-ttu-id="1124c-203">Uma sombra suspensa é aplicada a imagens por padrão.</span><span class="sxs-lookup"><span data-stu-id="1124c-203">A drop shadow is applied to images by default.</span></span>

## <a name="registering-your-thumbnail-handler"></a><span data-ttu-id="1124c-204">Registrando seu manipulador de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1124c-204">Registering Your Thumbnail Handler</span></span>

<span data-ttu-id="1124c-205">O registro de um manipulador de miniaturas baseia-se nas associações de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="1124c-205">Registration of a thumbnail handler is based on standard file associations.</span></span>

<span data-ttu-id="1124c-206">O GUID para a extensão do shell do manipulador de miniaturas é `E357FCCD-A995-4576-B01F-234630154E96` .</span><span class="sxs-lookup"><span data-stu-id="1124c-206">The GUID for the thumbnail handler Shell extension is `E357FCCD-A995-4576-B01F-234630154E96`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1124c-207">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1124c-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1124c-208">**Manipuladordeminiaturai**</span><span class="sxs-lookup"><span data-stu-id="1124c-208">**IThumbnailProvider**</span></span>](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[<span data-ttu-id="1124c-209">Criando manipuladores de miniatura</span><span class="sxs-lookup"><span data-stu-id="1124c-209">Building Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="1124c-210">Diretrizes do manipulador de miniaturas</span><span class="sxs-lookup"><span data-stu-id="1124c-210">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



