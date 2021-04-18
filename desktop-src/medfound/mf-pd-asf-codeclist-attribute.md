---
description: Contém informações sobre os codecs e formatos que foram usados para codificar o conteúdo em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de lista de codecs no cabeçalho ASF, definido na especificação ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Atributo MF_PD_ASF_CODECLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763915"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>\_Atributo de codec MF PD \_ asflist \_

Contém informações sobre os codecs e formatos que foram usados para codificar o conteúdo em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de lista de codecs no cabeçalho ASF, definido na especificação ASF.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo a partir do objeto de lista de codec no cabeçalho ASF. Um aplicativo que usa a [fonte de mídia ASF](asf-media-source.md) pode obter esse atributo chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) e obtendo o atributo do descritor de apresentação.

A tabela a seguir mostra o layout do blob de atributo.



| Campo de objeto da lista de codecs | Tipo de dados    | Tamanho    | Descrição                           |
|-------------------------|--------------|---------|---------------------------------------|
| Contagem de entradas de codec     | **DWORD**    | 4 bytes | Número de codecs                      |
| Entradas de codec           | **MINUCIOSA**\[\] | Varia  | Matriz de estruturas de informações de codec |



 

O campo entradas de código é uma matriz de estruturas. A tabela a seguir mostra o formato de cada entrada:



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo de objeto da lista de codecs</th>
<th>Tipo de dados</th>
<th>Tamanho</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Type</td>
<td><strong>DWORD</strong></td>
<td>4 bytes</td>
<td>Tipo de codec. Esse valor pode ser um dos seguintes:<br/>
<ul>
<li>0x0001: codec de áudio</li>
<li>0x0002: codec de vídeo</li>
<li>0xFFFF: desconhecido</li>
</ul></td>
</tr>
<tr class="even">
<td>Comprimento do nome do codec</td>
<td><strong>DWORD</strong></td>
<td>4 bytes</td>
<td>Tamanho da cadeia de caracteres do nome do codec, em bytes, incluindo o caractere <strong>nulo</strong> .</td>
</tr>
<tr class="odd">
<td>Nome do codec</td>
<td><strong>WCHAR</strong>[]</td>
<td>Varia</td>
<td>Cadeia de caracteres Unicode terminada em nulo que contém o nome do codec, como o &quot; Windows Media Video 9 &quot; .</td>
</tr>
<tr class="even">
<td>Tamanho da descrição do codec</td>
<td><strong>DWORD</strong></td>
<td>4 bytes</td>
<td>Tamanho da cadeia de caracteres de descrição do codec, em bytes, incluindo o caractere <strong>nulo</strong> .</td>
</tr>
<tr class="odd">
<td>Descrição do codec</td>
<td><strong>WCHAR</strong>[]</td>
<td>Varia</td>
<td>Uma cadeia de caracteres Unicode terminada em nulo que contém uma descrição do codec.</td>
</tr>
<tr class="even">
<td>Comprimento das informações do codec</td>
<td><strong>DWORD</strong></td>
<td>4 bytes</td>
<td>Tamanho do campo de informações do codec, em bytes.</td>
</tr>
<tr class="odd">
<td>Informações do codec</td>
<td><strong>Byte</strong>[]</td>
<td>Varia</td>
<td>Dados de codec. O significado desses dados depende do codec. Normalmente, esses dados indicam o formato.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> O layout do blob de atributo não corresponde exatamente ao layout do objeto de lista de codec no cabeçalho ASF. Em particular, os comprimentos de cadeia de caracteres são fornecidos em bytes e incluem o tamanho do terminador **nulo** .

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




