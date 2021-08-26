---
title: Adicionando uma lista de reprodução
description: Adicionando uma lista de reprodução
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- Criando capas, listas de reprodução
- Windows Media Player capas, listas de reprodução
- capas, listas de reprodução
- listas de reprodução, capas
- listas de reprodução de metarquivo, capas
- Windows Listas de reprodução de metarquivo de mídia, capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23d9198f1f913b83cef40cea9f6ec47976f9f1e08a5e54257ab16df63e538b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031586"
---
# <a name="adding-a-playlist"></a>Adicionando uma lista de reprodução

Você pode usar as listas de reprodução para escolher entre coleções de áudio e vídeo.

Usando a arte de sua primeira capa, você pode fazer algumas alterações no arquivo de definição de capa.

A primeira etapa é usar o shell que será usado para a maioria das capas:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



Agora, adicione uma segunda **exibição**, que contém uma lista de reprodução. Coloque o código a seguir após o </VIEW> do código do Shell.


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



Você precisará dar a essa segunda exibição uma ID para que possa consultá-la mais tarde. Adicione um PLAYelement e um STOPelement. Esses botões predefinidos facilitam a vida.


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



Por fim, adicione um evento OnClick ao PLAYelement para exibir uma lista de reprodução no segundo modo de exibição:


```C++
            onClick = "JScript: theme.openView('playview');" />

```



Você pode ver uma capa de playlist de trabalho semelhante na seção de exemplo do SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de criação de capa**](skin-creation-guide.md)
</dt> </dl>

 

 




