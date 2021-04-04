---
title: Exemplo de arquivo SAMI
description: Exemplo de arquivo SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- Arquivos SAMI (intercâmbio de mídia acessível) sincronizados
- SAMI (sincronizado com o intercâmbio de mídia acessível), arquivos
- SAMI (intercâmbio de mídia acessível), código de exemplo
- SAMI (sincronizado com o intercâmbio de mídia acessível), código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103837573"
---
# <a name="sami-file-example"></a><span data-ttu-id="54216-114">Exemplo de arquivo SAMI</span><span class="sxs-lookup"><span data-stu-id="54216-114">SAMI File Example</span></span>

<span data-ttu-id="54216-115">O código de exemplo a seguir é um arquivo SAMI completo com um conjunto de texto de legenda oculta e várias declarações de classe para o estilo de texto e a linguagem de legenda.</span><span class="sxs-lookup"><span data-stu-id="54216-115">The following example code is a complete SAMI file with one set of closed caption text and several class declarations for text style and caption language.</span></span>


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



<span data-ttu-id="54216-116">Os estilos definidos em um arquivo SAMI estão de acordo com a sintaxe padrão do seletor de CSS para elementos, classes e IDs.</span><span class="sxs-lookup"><span data-stu-id="54216-116">Styles defined within a SAMI file conform to standard CSS selector syntax for elements, classes, and IDs.</span></span> <span data-ttu-id="54216-117">No elemento BODY, todos os elementos P têm o estilo definido para o seletor de elemento P no elemento STYLE.</span><span class="sxs-lookup"><span data-stu-id="54216-117">In the BODY element, all P elements have the style defined for the P element selector in the STYLE element.</span></span> <span data-ttu-id="54216-118">O atributo Class de um elemento Especifica o idioma desse elemento, conforme definido pelos seletores de classe no elemento STYLE (os seletores que começam com pontos).</span><span class="sxs-lookup"><span data-stu-id="54216-118">The class attribute of an element specifies the language of that element as defined by the class selectors in the STYLE element (the selectors beginning with periods).</span></span> <span data-ttu-id="54216-119">Os nomes de idiomas especificados pelos seletores de classe podem ser qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="54216-119">The language names specified by the class selectors can be any string.</span></span> <span data-ttu-id="54216-120">Elementos com o atributo ID especificado têm estilo adicional aplicado conforme indicado pelos seletores de ID no elemento STYLE (os seletores prefixados com \# caracteres).</span><span class="sxs-lookup"><span data-stu-id="54216-120">Elements with the ID attribute specified have additional styling applied as indicated by the ID selectors in the STYLE element (the selectors prefixed with \# characters).</span></span>

<span data-ttu-id="54216-121">Quando usado em conjunto com o modelo de objeto do Windows Media Player, os seletores de classe correspondem ao *ClosedCaption*. Propriedade **SAMILang** , que pode ser usada para especificar o idioma das legendas.</span><span class="sxs-lookup"><span data-stu-id="54216-121">When used in conjunction with the Windows Media Player object model, the class selectors correspond to the *ClosedCaption*.**SAMILang** property, which can be used to specify the language of the captions.</span></span> <span data-ttu-id="54216-122">Os seletores de ID correspondem ao *ClosedCaption*. A propriedade **samistyle** , que pode ser usada para especificar o estilo no qual as legendas aparecerão.</span><span class="sxs-lookup"><span data-stu-id="54216-122">The ID selectors correspond to the *ClosedCaption*.**SAMIStyle** property, which can be used to specify the style the captions will appear in.</span></span>

<span data-ttu-id="54216-123">Para obter mais informações sobre como criar arquivos SAMI, consulte Understanding SAMI 1,0 no [site da Microsoft](/documentation/).</span><span class="sxs-lookup"><span data-stu-id="54216-123">For more information about creating SAMI files, see Understanding SAMI 1.0 at the [Microsoft website](/documentation/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="54216-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54216-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54216-125">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="54216-125">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 