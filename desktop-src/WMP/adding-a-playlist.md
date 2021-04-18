---
title: Adicionando uma lista de reprodução
description: Adicionando uma lista de reprodução
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- Criando capas, listas de reprodução
- Capas do Windows Media Player, listas de reprodução
- capas, listas de reprodução
- listas de reprodução, capas
- listas de reprodução de metarquivo, capas
- Listas de reprodução do metarquivo do Windows Media, capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796449"
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

 

 




