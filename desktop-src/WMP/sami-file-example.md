---
title: Exemplo de arquivo SAMI
description: Exemplo de arquivo SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Windows Media Player,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player de objeto, SAMI (Synchronized Accessible Media Interchange)
- modelo de objeto, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player ActiveX controle,SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Controle ActiveX dispositivo móvel, SAMI (Synchronized Accessible Media Interchange)
- ActiveX controle,SAMI (Synchronized Accessible Media Interchange)
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), arquivos
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), arquivos
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), código de exemplo
- SAMI (Intercâmbio de Mídia Acessível Sincronizado), código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d4e2ab5189f99118afae3fb2dae7374323cc8c16605bb458a04bd31810ed91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569802"
---
# <a name="sami-file-example"></a>Exemplo de arquivo SAMI

O código de exemplo a seguir é um arquivo SAMI completo com um conjunto de texto de legenda fechada e várias declarações de classe para o estilo de texto e o idioma da legenda.


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



Os estilos definidos em um arquivo SAMI estão em conformidade com a sintaxe do seletor CSS padrão para elementos, classes e IDs. No elemento BODY, todos os elementos P têm o estilo definido para o seletor de elemento P no elemento STYLE. O atributo de classe de um elemento especifica o idioma desse elemento conforme definido pelos seletores de classe no elemento STYLE (os seletores que começam com os períodos). Os nomes de idioma especificados pelos seletores de classe podem ser qualquer cadeia de caracteres. Elementos com o atributo ID especificado têm estilo adicional aplicado conforme indicado pelos seletores de ID no elemento STYLE (os seletores prefixados com \# caracteres).

Quando usados em conjunto com o modelo Windows Media Player objeto, os seletores de classe correspondem ao *ClosedCaption*. **Propriedade SAMILang,** que pode ser usada para especificar o idioma das legendas. Os seletores de ID correspondem *ao ClosedCaption.* **Propriedade SAMIStyle,** que pode ser usada para especificar o estilo em que as legendas aparecerão.

Para obter mais informações sobre como criar arquivos SAMI, consulte Noções básicas sobre o SAMI 1.0 no [site da Microsoft.](/documentation/)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 