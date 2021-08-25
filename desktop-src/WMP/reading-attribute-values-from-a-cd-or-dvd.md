---
title: Lendo valores de atributo de um CD ou DVD
description: Lendo valores de atributo de um CD ou DVD
ms.assetid: 441916fb-f66d-4a12-a95c-b47561c93e64
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
ms.openlocfilehash: 800fda1bf3002f015873b69e29503ecba637a978bac1b167724c04f5f15228b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861766"
---
# <a name="reading-attribute-values-from-a-cd-or-dvd"></a>Lendo valores de atributo de um CD ou DVD

Ao longo deste tópico, o **objeto Player** foi definido da seguinte maneira:


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



O código de exemplo C# a seguir recupera os valores de todos os atributos no disco atual que está na unidade e os grava em um arquivo.


```C++
private void logDiscAttributes()
{
    int iCDCount = 0; // Count of CD and DVD drives
    int iAttrCount = 0; // Attribute count.
    int iPLCount = 0; // Playlist item count.

    IWMPCdromCollection cdCollection;
    IWMPPlaylist playlist;
    IWMPMedia media;
    string strAttribName = "";
    string strAttribValue = "";
    string strText = "";

    // Create a StreamWriter object to write
    // the output to a file.
    StreamWriter sw = new StreamWriter(strOutFile, true);

    cdCollection = Player.cdromCollection;
    iCDCount = cdCollection.count;

    // Loop through the CD and DVD drives.
    for (int i = 0; i < iCDCount; i++)
    {
        playlist = cdCollection.Item(i).Playlist;

        // Loop through the playlist attributes.
        iAttrCount = playlist.attributeCount;
        for (int j = 0; j < iAttrCount; j++)
        {
            strText += "Playlist Attribute: \t";
            strAttribName = playlist.get_attributeName(j);
            strText += "\t" + strAttribName + "\t";
            strAttribValue = playlist.getItemInfo(strAttribName);
            strText += strAttribValue + "\n";
        }

        // Loop through the playlist.
        iPLCount = playlist.count;
        for (int k = 0; k < iPLCount; k++)
        {
            media = playlist.get_Item(k);

            // Loop through the media attributes.
            iAttrCount = media.attributeCount;
            for (int m = 0; m < iAttrCount; m++)
            {
                strText += "Track or Chapter [" + m.ToString() + "]";
                strAttribName = media.getAttributeName(m);
                strText += "\t" + strAttribName + "\t";
                strText += "Read Only: " + media.isReadOnlyItem(strAttribName) + "\t";
                strAttribValue = media.getItemInfo(strAttribName);
                strText += strAttribValue + "\n";
            }
        }
    }

    sw.Write(strText);
    sw.Close();

    MessageBox.Show(strOutFile + " created");
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos de item de mídia**](media-item-attributes.md)
</dt> <dt>

[**Objeto de mídia**](media-object.md)
</dt> </dl>

 

 




