---
title: Elemento PARAM (SDK do WMP)
description: O elemento PARAM define um parâmetro personalizado associado a uma playlist ou a um elemento de uma playlist.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Elemento PARAM Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811442"
---
# <a name="param-element"></a><span data-ttu-id="0b13a-104">Elemento PARAM</span><span class="sxs-lookup"><span data-stu-id="0b13a-104">PARAM Element</span></span>

<span data-ttu-id="0b13a-105">O elemento **param** define um parâmetro personalizado associado a uma playlist ou a um elemento de uma playlist.</span><span class="sxs-lookup"><span data-stu-id="0b13a-105">The **PARAM** element defines a custom parameter associated with a playlist or an element of a playlist.</span></span>

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a><span data-ttu-id="0b13a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b13a-106">Parameters</span></span>

<span data-ttu-id="0b13a-107">Um parâmetro também pode ser associado a show em vez de um clipe individual, colocando esse elemento diretamente após a tag **ASX** .</span><span class="sxs-lookup"><span data-stu-id="0b13a-107">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="0b13a-108">Esses itens são referenciados por seus nomes e um valor de índice que começa com zero.</span><span class="sxs-lookup"><span data-stu-id="0b13a-108">These items are referenced by their names and an index value beginning with zero.</span></span>

> [!Note]  
> <span data-ttu-id="0b13a-109">Este elemento **ASX** só está disponível para o Windows Media Player versão 6, 1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="0b13a-109">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="0b13a-110">A instalação padrão do Microsoft Internet Explorer 5 inclui uma versão compatível do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0b13a-110">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

 

## <a name="attributes"></a><span data-ttu-id="0b13a-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="0b13a-111">Attributes</span></span>

<span data-ttu-id="0b13a-112">**NOME**</span><span class="sxs-lookup"><span data-stu-id="0b13a-112">**NAME**</span></span>

<span data-ttu-id="0b13a-113">Nome usado para acessar o valor do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0b13a-113">Name used to access the parameter value.</span></span> <span data-ttu-id="0b13a-114">O nome pode ser qualquer cadeia de caracteres válida.</span><span class="sxs-lookup"><span data-stu-id="0b13a-114">The name can be any valid string.</span></span> <span data-ttu-id="0b13a-115">As cadeias de caracteres a seguir já foram definidas.</span><span class="sxs-lookup"><span data-stu-id="0b13a-115">The following strings have already been defined.</span></span>



| <span data-ttu-id="0b13a-116">String</span><span class="sxs-lookup"><span data-stu-id="0b13a-116">String</span></span>                          | <span data-ttu-id="0b13a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b13a-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b13a-118">AllowShuffle</span><span class="sxs-lookup"><span data-stu-id="0b13a-118">AllowShuffle</span></span>                    | <span data-ttu-id="0b13a-119">O atributo **Value** especifica se a lista de reprodução de metarquivo permite que o recurso de ordem aleatória do Windows Media Player reproduza as entradas em ordem aleatória.</span><span class="sxs-lookup"><span data-stu-id="0b13a-119">The **VALUE** attribute specifies whether the metafile playlist allows the Windows Media Player shuffle feature to play the entries in random order.</span></span> <span data-ttu-id="0b13a-120">O atributo **Value** pode ser definido como "Yes" ou "no".</span><span class="sxs-lookup"><span data-stu-id="0b13a-120">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="0b13a-121">O valor padrão é "no".</span><span class="sxs-lookup"><span data-stu-id="0b13a-121">The default value is "No".</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0b13a-122">Canusar</span><span class="sxs-lookup"><span data-stu-id="0b13a-122">CanPause</span></span>                        | <span data-ttu-id="0b13a-123">O atributo **Value** especifica se o usuário pode pausar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="0b13a-123">The **VALUE** attribute specifies whether the user can pause playback.</span></span> <span data-ttu-id="0b13a-124">O atributo **Value** pode ser definido como "Yes" ou "no".</span><span class="sxs-lookup"><span data-stu-id="0b13a-124">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="0b13a-125">O valor padrão é "Sim".</span><span class="sxs-lookup"><span data-stu-id="0b13a-125">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0b13a-126">CanSeek</span><span class="sxs-lookup"><span data-stu-id="0b13a-126">CanSeek</span></span>                         | <span data-ttu-id="0b13a-127">O atributo **Value** especifica se o usuário pode alterar a posição de reprodução atual usando a barra de busca, o avanço rápido ou a inversa rápida.</span><span class="sxs-lookup"><span data-stu-id="0b13a-127">The **VALUE** attribute specifies whether the user can change the current playback position by using the seek bar, fast forward, or fast reverse.</span></span> <span data-ttu-id="0b13a-128">O atributo **Value** pode ser definido como "Yes" ou "no".</span><span class="sxs-lookup"><span data-stu-id="0b13a-128">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="0b13a-129">O valor padrão é "Sim".</span><span class="sxs-lookup"><span data-stu-id="0b13a-129">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="0b13a-130">CanSkipBack</span><span class="sxs-lookup"><span data-stu-id="0b13a-130">CanSkipBack</span></span>                     | <span data-ttu-id="0b13a-131">O atributo **Value** especifica se o usuário pode pular para o item de playlist anterior clicando em **anterior**.</span><span class="sxs-lookup"><span data-stu-id="0b13a-131">The **VALUE** attribute specifies whether the user can skip backward to the previous playlist item by clicking **Previous**.</span></span> <span data-ttu-id="0b13a-132">O atributo **Value** pode ser definido como "Yes" ou "no".</span><span class="sxs-lookup"><span data-stu-id="0b13a-132">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="0b13a-133">O valor padrão é "Sim".</span><span class="sxs-lookup"><span data-stu-id="0b13a-133">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="0b13a-134">CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="0b13a-134">CanSkipForward</span></span>                  | <span data-ttu-id="0b13a-135">O atributo **Value** especifica se o usuário pode pular para o próximo item da playlist clicando em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="0b13a-135">The **VALUE** attribute specifies whether the user can skip forward to the next playlist item by clicking **Next**.</span></span> <span data-ttu-id="0b13a-136">O atributo **Value** pode ser definido como "Yes" ou "no".</span><span class="sxs-lookup"><span data-stu-id="0b13a-136">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="0b13a-137">O valor padrão é "Sim".</span><span class="sxs-lookup"><span data-stu-id="0b13a-137">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0b13a-138">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="0b13a-138">CPRadioID</span></span>                       | <span data-ttu-id="0b13a-139">O atributo **Value** especifica a ID de um feed de rádio fornecido por um repositório online tipo 1.</span><span class="sxs-lookup"><span data-stu-id="0b13a-139">The **VALUE** attribute specifies the ID of a radio feed provided by a type 1 online store.</span></span> <span data-ttu-id="0b13a-140">Ou seja, o atributo **Value** deve ser igual ao campo radioid de um dos feeds de rádio no catálogo da loja online.</span><span class="sxs-lookup"><span data-stu-id="0b13a-140">That is, the **VALUE** attribute must be equal to the RadioID field of one of the radio feeds in the online store's catalog.</span></span> <span data-ttu-id="0b13a-141">O elemento pai é o elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="0b13a-141">The parent element is the **ASX** element.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="0b13a-142">Codificação</span><span class="sxs-lookup"><span data-stu-id="0b13a-142">Encoding</span></span>                        | <span data-ttu-id="0b13a-143">O atributo **Value** é definido como "UTF-8" para indicar que o metarquivo é um arquivo codificado Unicode (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="0b13a-143">The **VALUE** attribute is set to "utf-8" to indicate that the metafile is a Unicode (UTF-8) encoded file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="0b13a-144">HtmlFlink</span><span class="sxs-lookup"><span data-stu-id="0b13a-144">HtmlFlink</span></span>                       | <span data-ttu-id="0b13a-145">O atributo **Value** é uma cadeia de caracteres fornecida por um repositório online tipo 1.</span><span class="sxs-lookup"><span data-stu-id="0b13a-145">The **VALUE** attribute is a string provided by a type 1 online store.</span></span> <span data-ttu-id="0b13a-146">O Windows Media Player passa a cadeia de caracteres para o método [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , que é implementado pelo plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="0b13a-146">Windows Media Player passes the string to the [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="0b13a-147">O método **GetItemInfo** retorna a URL da página da Web a ser exibida no painel em **execução** do Player.</span><span class="sxs-lookup"><span data-stu-id="0b13a-147">The **GetItemInfo** method returns the URL of the webpage to display in the **Now Playing** pane of the Player.</span></span> <span data-ttu-id="0b13a-148">A página da Web tem acesso a todos os métodos que o objeto **externo** expõe para armazenamentos do tipo 1.</span><span class="sxs-lookup"><span data-stu-id="0b13a-148">The webpage has access to all of the methods that the **External** object exposes to type 1 stores.</span></span> <span data-ttu-id="0b13a-149">Para obter uma lista desses métodos, consulte [external Object for tipo 1 online Stores](external-object-for-type-1-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="0b13a-149">For a list of those methods, see [External Object for Type 1 Online Stores](external-object-for-type-1-online-stores.md).</span></span> |
| <span data-ttu-id="0b13a-150">HTMLView</span><span class="sxs-lookup"><span data-stu-id="0b13a-150">HTMLView</span></span>                        | <span data-ttu-id="0b13a-151">O atributo **Value** especifica uma URL que é exibida no painel em **execução** do player de modo completo pela duração da lista de reprodução ou da entrada atual, dependendo se o elemento pai é o elemento **ASX** ou um elemento de **entrada** .</span><span class="sxs-lookup"><span data-stu-id="0b13a-151">The **VALUE** attribute specifies a URL that displays in the **Now Playing** pane of the full mode Player for the duration of the playlist or the current entry depending on whether the parent element is the **ASX** element or an **ENTRY** element.</span></span> <span data-ttu-id="0b13a-152">HTMLView não tem suporte para o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0b13a-152">HTMLView is not supported for the Windows Media Player control.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0b13a-153">Log:*FieldName* \[ :*namespace*\]</span><span class="sxs-lookup"><span data-stu-id="0b13a-153">Log:*FieldName*\[:*NameSpace*\]</span></span> | <span data-ttu-id="0b13a-154">O atributo **Value** especifica o valor para o qual o campo de log indicado será definido.</span><span class="sxs-lookup"><span data-stu-id="0b13a-154">The **VALUE** attribute specifies the value that the indicated log field will be set to.</span></span> <span data-ttu-id="0b13a-155">A parte:*namespace* do atributo **Name** é opcional.</span><span class="sxs-lookup"><span data-stu-id="0b13a-155">The :*NameSpace* portion of the **NAME** attribute is optional.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="0b13a-156">Antes do buffer</span><span class="sxs-lookup"><span data-stu-id="0b13a-156">Prebuffer</span></span>                       | <span data-ttu-id="0b13a-157">O atributo **Value** especifica se a próxima entrada da playlist começa a ser armazenada em buffer antes do final da entrada atual, o que permite uma transição direta.</span><span class="sxs-lookup"><span data-stu-id="0b13a-157">The **VALUE** attribute specifies whether the next playlist entry begins buffering before the end of the current entry, which enables a seamless transition.</span></span> <span data-ttu-id="0b13a-158">O atributo **Value** pode ser definido como "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="0b13a-158">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0b13a-159">ShowWhileBuffering</span><span class="sxs-lookup"><span data-stu-id="0b13a-159">ShowWhileBuffering</span></span>              | <span data-ttu-id="0b13a-160">O atributo **Value** especifica se um arquivo de imagem referenciado pelo elemento de **entrada** atual continua a ser exibido após o tempo de duração especificado, enquanto a próxima entrada de playlist é armazenada em buffer.</span><span class="sxs-lookup"><span data-stu-id="0b13a-160">The **VALUE** attribute specifies whether an image file referenced by the current **ENTRY** element continues to display past its specified duration time while the next playlist entry is buffered.</span></span> <span data-ttu-id="0b13a-161">O atributo **Value** pode ser definido como "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="0b13a-161">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="0b13a-162">**VALUE**</span><span class="sxs-lookup"><span data-stu-id="0b13a-162">**VALUE**</span></span>

<span data-ttu-id="0b13a-163">Valor associado a esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0b13a-163">Value associated with this parameter.</span></span> <span data-ttu-id="0b13a-164">Pode ser um valor numérico ou de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0b13a-164">It can be either a numeric or string value.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="0b13a-165">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="0b13a-165">Parent/Child Elements</span></span>



| <span data-ttu-id="0b13a-166">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="0b13a-166">Hierarchy</span></span>       | <span data-ttu-id="0b13a-167">Elementos</span><span class="sxs-lookup"><span data-stu-id="0b13a-167">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="0b13a-168">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0b13a-168">Parent elements</span></span> | <span data-ttu-id="0b13a-169">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="0b13a-169">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="0b13a-170">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0b13a-170">Child elements</span></span>  | <span data-ttu-id="0b13a-171">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0b13a-171">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="0b13a-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b13a-172">Remarks</span></span>

<span data-ttu-id="0b13a-173">Esse elemento permite que os usuários coloquem informações adicionais sobre cada clipe dentro do elemento de **entrada** que o contém.</span><span class="sxs-lookup"><span data-stu-id="0b13a-173">This element allows users to place additional information about each clip inside the **ENTRY** element that contains it.</span></span> <span data-ttu-id="0b13a-174">Para recuperar as informações de metadados especificadas na **entrada** da playlist, use a *mídia*. método **getItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="0b13a-174">To retrieve metadata information specified in the playlist **ENTRY**, use the *Media*.**getItemInfo** method.</span></span> <span data-ttu-id="0b13a-175">A *mídia*. o método **getItemInfo** recupera o valor do atributo **Value** , dado o nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0b13a-175">The *Media*.**getItemInfo** method retrieves the value of the **VALUE** attribute, given the name of the parameter.</span></span> <span data-ttu-id="0b13a-176">As versões anteriores do Windows Media Player recuperam as informações de metadados especificadas na **entrada** da playlist, usando o método **GetMediaParameter** , dado o nome do parâmetro e um número de índice para a entrada.</span><span class="sxs-lookup"><span data-stu-id="0b13a-176">Previous versions of Windows Media Player retrieve metadata information specified in the playlist **ENTRY**, using the **GetMediaParameter** method given the name of the parameter and an index number for the entry.</span></span>

<span data-ttu-id="0b13a-177">Um parâmetro também pode ser associado a show em vez de um clipe individual, colocando esse elemento diretamente após a tag **ASX** .</span><span class="sxs-lookup"><span data-stu-id="0b13a-177">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="0b13a-178">Esses itens são referenciados por seus nomes e um valor de índice que começa com zero.</span><span class="sxs-lookup"><span data-stu-id="0b13a-178">These items are referenced by their names and an index value beginning with zero.</span></span>

<span data-ttu-id="0b13a-179">**Observação**</span><span class="sxs-lookup"><span data-stu-id="0b13a-179">**Note**</span></span>

<span data-ttu-id="0b13a-180">Este elemento **ASX** só está disponível para o Windows Media Player versão 6, 1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="0b13a-180">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="0b13a-181">A instalação padrão do Microsoft Internet Explorer 5 inclui uma versão compatível do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0b13a-181">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="0b13a-182">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b13a-182">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="0b13a-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b13a-183">Requirements</span></span>



| <span data-ttu-id="0b13a-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b13a-184">Requirement</span></span> | <span data-ttu-id="0b13a-185">Valor</span><span class="sxs-lookup"><span data-stu-id="0b13a-185">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b13a-186">Versão</span><span class="sxs-lookup"><span data-stu-id="0b13a-186">Version</span></span><br/> | <span data-ttu-id="0b13a-187">O Windows Media Player versão 7,0 ou posterior, o Windows Media Player 9 Series ou posterior é necessário para os atributos de nome predefinidos, o Windows Media Player 10 ou posterior é necessário para os nomes predefinidos CanPause, CanSeek, CanSkipBack e CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="0b13a-187">Windows Media Player version 7.0 or later, Windows Media Player 9 Series or later is required for the predefined NAME attributes, Windows Media Player 10 or later is required for the predefined names CanPause, CanSeek, CanSkipBack, and CanSkipForward</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b13a-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b13a-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b13a-189">**Exibindo páginas da Web no Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="0b13a-189">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="0b13a-190">**Log de dados de fluxo**</span><span class="sxs-lookup"><span data-stu-id="0b13a-190">**Logging Stream Data**</span></span>](logging-stream-data.md)
</dt> <dt>

[<span data-ttu-id="0b13a-191">**Referência de elementos de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0b13a-191">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="0b13a-192">**Referência do metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="0b13a-192">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





