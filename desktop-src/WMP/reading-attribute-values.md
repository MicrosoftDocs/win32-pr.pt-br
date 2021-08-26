---
title: Lendo valores de atributo
description: Lendo valores de atributo
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
keywords:
- Windows Media Player atributos para itens de mídia
- Windows Media Player modelo de objeto, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Dispositivo móvel, atributos para itens de mídia
- Windows Media Player ActiveX controle,atributos para itens de mídia
- Windows Media Player Controle ActiveX dispositivo móvel, atributos para itens de mídia
- ActiveX controle,atributos para itens de mídia
- Windows Media Player biblioteca, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, valores de leitura
- lendo valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8431405b68435f41cb357a810e30c37bb96c5971824b3878b1982986aa0d0833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002826"
---
# <a name="reading-attribute-values"></a>Lendo valores de atributo

Os atributos que você pode encontrar na biblioteca e nos arquivos Windows Mídia têm nomes predefinidos. Você pode escrever um código que recupera o valor de um atributo passando o nome desse atributo para *Mídia*. **getItemInfo** ou *Media*. **getItemInfoByType**. Você também pode escrever código que recupera os valores de todos os atributos em um arquivo ou item.

O exemplo C# a seguir recupera o valor do atributo **Title** e o exibe em uma caixa de mensagem. Neste exemplo, o **objeto Player** foi definido como axWMPLib.AxWindowsMediaPlayer Player.


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



Na chamada para **getItemInfoByType**, o segundo parâmetro é uma cadeia de caracteres que especifica o idioma. Se você passar uma cadeia de caracteres vazia, conforme mostrado neste exemplo, o método recuperará o valor no idioma padrão. Para obter informações sobre o terceiro parâmetro, consulte [Atributos com vários valores](attributes-with-multiple-values.md).

O exemplo de C# a seguir recupera os valores de um determinado atributo no item de mídia atual. Ele retorna esses valores como uma cadeia de caracteres delimitada por ponto e vírgula. Observe que, para atributos representados como objetos, como **WM/Synchronizado, \_** **WM/Picture** e **WM/UserWebURL,** a função retorna uma cadeia de caracteres vazia.


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



O terceiro argumento passado para o **método getItemInfoByType** é o índice de um atributo específico em um conjunto de atributos com o mesmo nome.

Você pode usar código semelhante para recuperar atributos que têm nomes exclusivos. Nesses casos, **getAttributeCountByType** retorna 1. No exemplo mostrado anteriormente, a chamada para **getItemInfoByType** seria executada apenas uma vez.

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

 

 




