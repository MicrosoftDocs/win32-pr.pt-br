---
description: A interface IMediaDet recupera informações sobre um arquivo de mídia, como o número de fluxos, o tipo de mídia, a duração e a taxa de quadros de cada fluxo.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interface IMediaDet (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782231"
---
# <a name="imediadet-interface"></a>Interface IMediaDet

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IMediaDet` interface recupera informações sobre um arquivo de mídia, como o número de fluxos, o tipo de mídia, a duração e a taxa de quadros de cada fluxo. Ele também contém métodos para recuperar quadros individuais de um fluxo de vídeo. O objeto do [detector de mídia (MediaDet)](media-detector--mediadet.md) expõe essa interface.

Para obter informações sobre um arquivo usando essa interface, execute as seguintes etapas:

1.  Crie uma instância do objeto MediaDet chamando **CoCreateInstance**. A ID de classe é CLSID \_ MediaDet.
2.  Chame [**IMediaDet::p \_ nome**](imediadet-put-filename.md) do arquivo UT para especificar o nome do arquivo de origem.
3.  Chame [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para obter o número de fluxos de saída na origem.
4.  Chame [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) para especificar um fluxo específico.
5.  Chame qualquer um dos seguintes métodos:
    -   [**IMediaDet:: obter a \_ taxa de quadros**](imediadet-get-framerate.md)
    -   [**IMediaDet:: obter \_ streamLength**](imediadet-get-streamlength.md)
    -   [**IMediaDet:: obter \_ StreamMediaType**](imediadet-get-streammediatype.md)
    -   [**IMediaDet:: obter \_ streamtype**](imediadet-get-streamtype.md)

Para recuperar um quadro de vídeo, chame [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md). O quadro retornado sempre está no formato RGB de 24 bits.

> [!Note]  
> Não use o mesmo objeto MediaDet com vários arquivos. Para obter informações ou quadros de vídeo de mais de um arquivo, use instâncias MediaDet separadas.

 

A interface **IMediaDet** não dá suporte a formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , portanto, você não pode usar essa interface para obter campos entrelaçados ou informações sobre entrelaçamento. Além disso, se o decodificador upstream der suporte apenas a **VIDEOINFOHEADER2**, você não poderá usar `IMediaDet` . Esse pode ser o caso com um decodificador MPEG-2, por exemplo. Além disso, a `IMediaDet` interface ignora todos os fluxos no arquivo que não são de vídeo ou áudio. Por exemplo, se o arquivo contiver um fluxo de áudio, um fluxo de dados e um fluxo de vídeo, o método **Get \_ OutputStreams** relatará apenas dois fluxos (o áudio e o vídeo).

## <a name="members"></a>Membros

A interface **IMediaDet** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMediaDet** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMediaDet** tem esses métodos.



| Método                                                        | Descrição                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)  | Alterna o detector de mídia para o modo de captura de bitmap e procura o grafo de filtro em um horário especificado.<br/> |
| [**obter \_ CurrentStream**](imediadet-get-currentstream.md)     | Recupera o número de fluxo usado atualmente pelo detector de mídia.<br/>                               |
| [**obter \_ nome de arquivo**](imediadet-get-filename.md)               | Recupera o nome do arquivo de origem usado atualmente pelo detector de mídia.<br/>                     |
| [**obter \_ filtro**](imediadet-get-filter.md)                   | Recupera um ponteiro para o filtro de origem usado atualmente pelo detector de mídia.<br/>                  |
| [**obter \_ taxa de quadros**](imediadet-get-framerate.md)             | Recupera a taxa de quadros do fluxo atual.<br/>                                                 |
| [**obter \_ OutputStreams**](imediadet-get-outputstreams.md)     | Recupera o número de fluxos de áudio e vídeo contidos na origem da mídia.<br/>                  |
| [**obter \_ streamLength**](imediadet-get-streamlength.md)       | Recupera a duração do fluxo atual.<br/>                                                   |
| [**obter \_ StreamMediaType**](imediadet-get-streammediatype.md) | Recupera o tipo de mídia do fluxo atual.<br/>                                                 |
| [**obter \_ streamtype**](imediadet-get-streamtype.md)           | Recupera o identificador global exclusivo (GUID) para o tipo de mídia do fluxo atual.<br/>       |
| [**obter \_ StreamTypeB**](imediadet-get-streamtypeb.md)         | Recupera uma cadeia de caracteres que representa o GUID do tipo de mídia para o fluxo atual.<br/>              |
| [**GetBitmapBits**](imediadet-getbitmapbits.md)              | Recupera um quadro de vídeo no tempo de mídia especificado.<br/>                                            |
| [**GetSampleGrabber**](imediadet-getsamplegrabber.md)        | Recupera um ponteiro para a interface [**ISampleGrabber**](isamplegrabber.md) .<br/>                  |
| [**colocar \_ CurrentStream**](imediadet-put-currentstream.md)     | Especifica o número de fluxo para o detector de mídia a ser usado.<br/>                                      |
| [**colocar \_ nome do arquivo**](imediadet-put-filename.md)               | Especifica o nome do arquivo de origem para o detector de mídia a ser usado.<br/>                            |
| [**colocar \_ filtro**](imediadet-put-filter.md)                   | Especifica um filtro de origem para o detector de mídia a ser usado.<br/>                                        |
| [**WriteBitmapBits**](imediadet-writebitmapbits.md)          | Recupera um quadro de vídeo no tempo de mídia especificado e grava-o em um arquivo.<br/>                    |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
