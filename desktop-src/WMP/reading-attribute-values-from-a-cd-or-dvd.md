---
title: Lendo valores de atributo de um CD ou DVD
description: Lendo valores de atributo de um CD ou DVD
ms.assetid: 441916fb-f66d-4a12-a95c-b47561c93e64
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
ms.openlocfilehash: 8909a752e9a974e4959be8ecd933d4bb3f1bfd4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292596"
---
# <a name="reading-attribute-values-from-a-cd-or-dvd"></a><span data-ttu-id="684a7-114">Lendo valores de atributo de um CD ou DVD</span><span class="sxs-lookup"><span data-stu-id="684a7-114">Reading Attribute Values from a CD or DVD</span></span>

<span data-ttu-id="684a7-115">Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="684a7-115">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="684a7-116">O código de exemplo C# a seguir recupera os valores de todos os atributos no disco atual que está na unidade e os grava em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="684a7-116">The following C# example code retrieves the values of all attributes in the current disc that is in the drive and writes them to a file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="684a7-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="684a7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="684a7-118">**Atributos de item de mídia**</span><span class="sxs-lookup"><span data-stu-id="684a7-118">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="684a7-119">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="684a7-119">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 




