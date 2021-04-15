---
description: Especifica os marcadores em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de marcador no cabeçalho ASF, definido na especificação ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: Atributo MF_PD_ASF_MARKER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761429"
---
# <a name="mf_pd_asf_marker-attribute"></a>\_Atributo de marcador MF PD \_ ASF \_

Especifica os marcadores em um arquivo ASF (Advanced Systems Format). Esse atributo corresponde ao objeto de marcador no cabeçalho ASF, definido na especificação ASF.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) cria o descritor de apresentação e gera esse atributo a partir do objeto Marker. A tabela a seguir mostra o formato do blob:



| Campo de objeto de marcador | Tipo de dados    | Tamanho    | Descrição       |
|---------------------|--------------|---------|-------------------|
| Contagem de marcadores       | **DWORD**    | 4 bytes | Número de marcadores |
| Marcadores             | **MINUCIOSA**\[\] | Varia  | Matriz de marcadores  |



 

A primeira **DWORD** é o número de marcadores, seguido por uma matriz de marcadores. Cada marcador tem o seguinte formato:



| Campo de objeto de marcador       | Tipo de dados     | Tamanho    | Descrição                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| Comprimento da descrição do marcador | **DWORD**     | 4 bytes | Tamanho da cadeia de caracteres de descrição, em bytes, incluindo o caractere nulo.           |
| Descrição do marcador        | **WCHAR**\[\] | Varia  | Cadeia de caracteres terminada em nulo que descreve o marcador.                                 |
| Tempo da apresentação         | **LONGLONG**  | 8 bytes | Hora da apresentação do marcador, em unidades de 100 a nanossegundos.                         |
| Hora de envio                 | **LONGLONG**  | 8 bytes | Hora de envio da entrada do marcador, em milissegundos.                                   |
| Deslocamento                    | **UINT64**    | 8 bytes | Deslocamento, em bytes, no objeto de dados que especifica a posição do mercado. |



 

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

 

 




