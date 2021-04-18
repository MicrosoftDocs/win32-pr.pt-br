---
title: Lendo valores de atributo
description: Lendo valores de atributo
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Windows Media Player, atributos para itens de mídia
- Modelo de objeto do Windows Media Player, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Mobile, atributos para itens de mídia
- Controle ActiveX do Windows Media Player, atributos para itens de mídia
- Controle ActiveX móvel do Windows Media Player, atributos para itens de mídia
- Controle ActiveX, atributos para itens de mídia
- Biblioteca do Windows Media Player, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, lendo valores
- lendo valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789230"
---
# <a name="reading-attribute-values"></a>Lendo valores de atributo

Os atributos que você pode encontrar na biblioteca e nos arquivos de mídia do Windows têm nomes predefinidos. Você pode escrever um código que recupere o valor de um atributo, passando o nome desse atributo para a *mídia*. **getItemInfo** ou *mídia*. **getItemInfoByType**. Você também pode escrever um código que recupere os valores de todos os atributos em um arquivo ou item.

O exemplo de C# a seguir recupera o valor do atributo **title** e o exibe em uma caixa de mensagem. Neste exemplo, o objeto **Player** foi definido como AxWMPLib. AxWindowsMediaPlayer Player.


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



Na chamada para **getItemInfoByType**, o segundo parâmetro é uma cadeia de caracteres que especifica o idioma. Se você passar uma cadeia de caracteres vazia, conforme mostrado neste exemplo, o método recuperará o valor no idioma padrão. Para obter informações sobre o terceiro parâmetro, consulte [atributos com vários valores](attributes-with-multiple-values.md).

O exemplo C# a seguir recupera os valores para um determinado atributo no item de mídia atual. Ele retorna esses valores como uma cadeia de caracteres delimitada por ponto e vírgula. Observe que, para os atributos representados como objetos, como o **WM/música \_ sincronizado**, o **WM/Picture** e o **WM/UserWebURL**, a função retorna uma cadeia de caracteres vazia.


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



O terceiro argumento passado para o método **getItemInfoByType** é o índice de um atributo específico em um conjunto de atributos com o mesmo nome.

Você pode usar um código semelhante para recuperar atributos que têm nomes exclusivos. Nesses casos, **getAttributeCountByType** retorna 1. No exemplo mostrado anteriormente, a chamada para **getItemInfoByType** seria executada apenas uma vez.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Alterando valores de atributo**](changing-attribute-values.md)
</dt> <dt>

[**Atributos de item de mídia**](media-item-attributes.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Lendo valores de atributo de um CD ou DVD**](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




