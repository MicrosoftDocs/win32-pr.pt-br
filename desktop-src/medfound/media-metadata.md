---
description: Metadados de mídia
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Metadados de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761566"
---
# <a name="media-metadata"></a>Metadados de mídia

Os arquivos de mídia contêm propriedades que descrevem o conteúdo do arquivo. No Microsoft Media Foundation, essas propriedades podem ser categorizadas da seguinte maneira:

-   **Atributos de tipo de mídia** especificam os parâmetros de codificação, como o algoritmo de codificação (subtipo de mídia), o tamanho do quadro de vídeo, a taxa de quadros de vídeo, a taxa de bits de áudio e a taxa de amostragem de áudio. Para obter mais informações sobre atributos de tipo de mídia, consulte [tipos de mídia](media-types.md).
-   Os **metadados** contêm informações descritivas para o conteúdo de mídia, como título, artista, compositor e gênero. Os metadados também podem descrever os parâmetros de codificação. Pode ser mais rápido acessar essas informações por meio de metadados do que por meio de atributos de tipo de mídia.
-   **As propriedades de DRM** contêm informações sobre restrições de uso. Atualmente Media Foundation não oferece suporte a propriedades de DRM por meio de metadados, com exceção da propriedade **PKEY \_ DRM \_ isproteged** .

Há duas maneiras de ler metadados em Media Foundation:

-   A interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (Media Foundation metadados da versão 1).
-   A interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) do shell do Windows (metadados do Shell).

Os metadados do Shell pertencem não apenas aos arquivos de mídia, mas a um intervalo muito maior de arquivos no sistema.

A tabela a seguir compara os recursos e as limitações de cada API de metadados.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metadados do Media Foundation v1</th>
<th>Metadados do Shell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Requer o Windows Vista ou posterior.</td>
<td>Requer o Windows 7.
<blockquote>
[!Note]<br />
Os metadados do Shell em geral não exigem o Windows 7, mas Media Foundation não dava suporte aos metadados do Shell antes do Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>As propriedades não são compatíveis com o sistema de propriedades do Shell.</td>
<td>As propriedades são compatíveis com o sistema de propriedades do Shell.</td>
</tr>
<tr class="odd">
<td>As propriedades podem ser aplicadas a todo o arquivo ou no nível do fluxo.</td>
<td>Há suporte apenas para propriedades em nível de arquivo. Não há suporte para propriedades em nível de fluxo.</td>
</tr>
<tr class="even">
<td>As propriedades podem ter valores em vários idiomas.</td>
<td>Não há suporte para valores em vários idiomas.</td>
</tr>
<tr class="odd">
<td>As chaves de propriedade são cadeias de caracteres largos.</td>
<td>As chaves de propriedade são valores de <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> .</td>
</tr>
<tr class="even">
<td>Os valores de propriedade são valores de <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</td>
<td>Os valores de propriedade são valores de <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                     | Descrição                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Provedores de metadados do Shell](shell-metadata-providers.md)<br/>                       | A partir do Windows 7, Media Foundation expõe os metadados por meio da interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .<br/> |
| [Propriedades de metadados para Arquivos de mídia](metadata-properties-for-media-files.md)<br/> | Este tópico lista as propriedades de metadados mais comuns para arquivos de mídia.<br/>                                                           |
| [Provedores de metadados no Windows Vista](metadata-providers-in-windows-vista.md)<br/> | No Windows Vista, Media Foundation expõe metadados por meio da interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .<br/>                   |



 

Se você estiver implementando uma fonte de mídia personalizada e quiser expor metadados do Shell, consulte [provedores de metadados personalizados para arquivos de mídia](custom-metadata-providers-for-media-files.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
