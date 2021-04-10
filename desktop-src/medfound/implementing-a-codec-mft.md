---
description: Este tópico fornece algumas diretrizes para implementar um decodificador ou um codificador como uma Media Foundation transformação (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementando uma MFT do codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171732"
---
# <a name="implementing-a-codec-mft"></a>Implementando uma MFT do codec

Este tópico fornece algumas diretrizes para implementar um decodificador ou um codificador como uma Media Foundation transformação (MFT).

-   [Codificadores](#encoders)
    -   [Negociação de formato do codificador](#encoder-format-negotiation)
-   [Decodificadores](#decoders)
    -   [Decodificadores somente de transcodificação](#transcode-only-decoders)
    -   [Atributos de telecineon](#telecine-attributes)
-   [Tópicos relacionados](#related-topics)

## <a name="encoders"></a>Codificadores

### <a name="encoder-format-negotiation"></a>Negociação de formato do codificador

O procedimento a seguir é usado para inicializar um codificador:

1.  Consulte o MFT para a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
2.  Chame [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para definir as propriedades de codificação.
3.  Chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o formato de codificação.
4.  Chame [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para obter uma lista de tipos de entrada compatíveis. (Essa etapa pode ser ignorada.)
5.  Chame [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o formato de entrada descompactado.

Depois que o tipo de saída é definido na etapa 3, o método [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) deve retornar uma lista de tipos de entrada que são compatíveis com o tipo de saída atual. Em outras palavras, todos os tipos retornados por **GetInputAvailableType** nesse ponto devem ser válidos para [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

Para decodificadores, a ordem na qual os tipos são definidos é invertida: o tipo de entrada é definido primeiro, seguido pelo tipo de saída. Depois que o tipo de entrada é definido, o método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) deve retornar uma lista de tipos que podem ser passados para o método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .

Os codificadores e os decodificadores devem dar suporte a NV12 como um formato descompactado comum. Isso garante que os componentes de pipeline possam interoperar com conversões mínimas do colorspace. É claro que outros formatos também podem ter suporte.

## <a name="decoders"></a>Decodificadores

### <a name="transcode-only-decoders"></a>Decodificadores de Transcode-Only

Alguns decodificadores são otimizados para transcodificação (decodificação e, em seguida, codificação de um fluxo) e não são adequados para uso durante a reprodução.

Se uma MFT do decodificador for destinada apenas para transcodificação, defina o sinalizador de **enumeração de MFT \_ \_ \_ \_ somente transcodificará** ao registrar o MFT. (Consulte [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)

Por padrão, os decodificadores de transcodificação não são retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . Para enumerar os decodificadores de transcodificação, chame **MFTEnumEx** e defina o sinalizador do **sinalizador de enumeração de MFT \_ \_ \_ \_ somente transcodificar** no parâmetro *flags* . Quando usado na função **MFTEnumEx** , esse sinalizador enumerava os decodificadores de transcodificação e outros decodificadores.



| **\_ \_ \_ \_ Somente transcodificação de sinalizador de enumeração de MFT** MFTRegister | **\_ \_ \_ \_ Somente transcodificação de sinalizador de enumeração de MFT** MFTEnumEx | MFT é enumerado? |
|--------------------------------------------------|------------------------------------------------|--------------------|
| 1                                                | 1                                              | Sim                |
| 1                                                | 0                                              | Não                 |
| 0                                                | 1                                              | Sim                |
| 0                                                | 0                                              | Sim                |



 

### <a name="telecine-attributes"></a>Atributos de telecineon

A origem da mídia pode anexar os seguintes atributos de telecineon aos exemplos de mídia que ele fornece.



| Atributo                                                                                   | Descrição                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md) | Equivalente ao sinalizador "repetir primeiro campo" (RFF). |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) | Inverso do sinalizador "Top Field First" (TFF).       |



 

Esses sinalizadores fornecem uma dica para o processador de vídeo avançado (EVR) quando ele executa o desentrelaçamento. Um decodificador deve propagar esses sinalizadores downstream copiando-os para os exemplos de saída, para que eles cheguem ao EVR.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravando uma MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 
