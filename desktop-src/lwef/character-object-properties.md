---
title: Propriedades do objeto Character
description: Propriedades do objeto Character
ms.assetid: 86748de2-f5c8-4057-bfa4-79d46cac1e62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c80e16bdb35d3fdfd8687eb15f200d2005ab75027e4dcc786f883d21232af4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610686"
---
# <a name="character-object-properties"></a>Propriedades do objeto Character

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O objeto [**Character**](/windows/desktop/lwef/the-characters-object) expõe as seguintes propriedades:

-   [**Ativo**](active-property.md)
-   [**AutoPopupMenu**](autopopupmenu-property.md)
-   [**Descrição**](description-property.md)
-   [**ExtraData**](extradata-property.md)
-   [**GUID**](guid-property.md)
-   [**HasOtherClients**](hasotherclients-property.md)
-   [**Altura**](height-property.md)
-   [**HelpContextid**](helpcontextid-property-ch.md)
-   [**HelpFile**](helpfile-property.md)
-   [**HelpModeOn**](helpmodeon-property.md)
-   [**Tempo ocioso**](idleon-property.md)
-   [**LanguageID**](languageid-property.md)
-   [**Mantida**](left-property.md)
-   [**MoveCause**](movecause-property.md)
-   [**Nome**](name-property.md)
-   [**OriginalHeight**](originalheight-property.md)
-   [**OriginalWidth**](originalwidth-property.md)
-   [**Densidade**](pitch-property.md)
-   [**SoundEffectsOn**](soundeffectson-property.md)
-   [**Rápida**](speed-property.md)
-   [**SRModeID**](srmodeid-property.md)
-   [**SRStatus**](srstatus-property.md)
-   [**Início**](top-property.md)
-   [**TTSModeID**](ttsmodeid-property.md)
-   [**Versão**](version-property.md)
-   [**VisibilityCause**](visibilitycause-property.md)
-   [**Visível**](visible-property-cob.md)
-   [**Largura**](width-property-co.md)

Observe que as propriedades [**altura**](height-property.md), [**esquerda**](left-property.md), [**superior**](top-property.md)e [**largura**](width-property-co.md) de um caractere diferem das que podem ser suportadas pelo ambiente de programação para o posicionamento do controle. As propriedades de [**caractere**](/windows/desktop/lwef/the-characters-object) se aplicam à apresentação visível de um caractere, não ao local do controle do Microsoft Agent.

Assim como acontece com métodos de objeto de [**caractere**](/windows/desktop/lwef/the-characters-object) , você pode acessar as propriedades de um caractere usando a coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) ou simplificar sua sintaxe declarando uma variável de objeto e definindo-a como um caractere na coleção. No exemplo a seguir, Test1 e test2 serão definidas com o mesmo valor:


```
   Dim Genie 
   Dim MyRequest
   
   Sub window_Onload

   Agent.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent.Characters("Genie")

   Genie.MoveTo 15,15
   Set MyRequest = Genie.Show()

   End Sub

   Sub Agent_RequestComplete(ByVal Request)

   If Request = MyRequest Then 
      Test1 = Agent.Characters("Genie").Top
      Test2 = Genie.Top
      MsgBox "Test 1 is " + cstr(Test1) + "and Test 2 is " + cstr(Test2)
   End If

   End Sub
```



Como o servidor carrega um caractere de forma assíncrona, verifique se o caractere foi carregado antes de consultar suas propriedades, por exemplo, usando o evento [**RequestComplete**](requestcomplete-event.md) . Caso contrário, as propriedades podem retornar valores incorretos.

 

 