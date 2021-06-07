---
description: Este tópico fornece informações sobre o codec JPEG nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Visão geral do formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444187"
---
# <a name="jpeg-format-overview"></a>Visão geral do formato JPEG

Este tópico fornece informações sobre o codec JPEG nativo disponível por meio do Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidade do Codec

A tabela a seguir fornece informações de identificação de codec.



|   Componente            | Descrição                             |
|------------------------|-----------------------------------------|
| Nomes formais         | JPEG |
| Extensões de nome de arquivo | jpe, jpeg, jpg                          |
| tipo MIME              | image/jpeg, image/jpe, image/jpg        |
| Suporte à especificação  | Especificação 1.02 do JFIF                 |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec JPEG.



| Componente        | Nome amigável             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato do contêiner | Contêiner \_ GUIDFormatJpeg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Decodificador          | CLSID \_ WICJpegDecoder     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Codificador          | CLSID \_ WICJpegEncoder     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Codificação

A API de codificação WIC foi projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções do codificador

Os codecs habilitados para WIC diferem no nível da opção de codificação. As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte a Visão geral [de codificação](-wic-creating-encoder.md).

O codec JPEG usa opções básicas do WIC. A tabela a seguir lista as opções do codificador WIC com suporte pelo codec jpeg nativo.



| Nome da propriedade                                        | Vartype           | Intervalo de valores                                                                       | Valor Padrão                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0 - 1.0                                                                           | 0,9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | VT \_ UI1           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Luminância](#luminance-option)                       | MATRIZ VT \_ UI4/VT \_ | 64 entradas (DCT)                                                                  | Tabela de luminância padrão.                                                       |
| [Crominância](#chrominance-option)                   | MATRIZ VT \_ UI4/VT \_ | 64 entradas (DCT)                                                                  | Tabela de chrominance padrão.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | VT \_ UI1           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | BOOL da VT \_          | **TRUE** / **FALSE**                                                                | **FALSE**                                                                      |



 

Se uma opção de codificador estiver presente na lista de opções [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) à qual o codec não dá suporte, ela será ignorada.

### <a name="imagequality-option"></a>Opção ImageQuality

Especifica a fidelidade da imagem desejada. 0,0 indica a fidelidade mais baixa possível e 1,0 especifica a fidelidade mais alta.

O valor padrão é 0,9.

### <a name="bitmaptransform-option"></a>Opção BitmapTransform

Especifica como a imagem deve ser transformada durante a decodificação da imagem. Essa opção deve ser definida como um dos valores de enumeração [**WICBitmapTransformOptions.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

O valor padrão é [**WICBitmapTransformRotate0.**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)

### <a name="luminance-option"></a>Opção Luminance

Especifica a tabela de nível de brilho de escala de cinza a ser usada para codificação.

### <a name="chrominance-option"></a>Opção Chrominance

Especifica a tabela de chrominance a ser usada para codificação.

### <a name="jpegycrcbsubsampling-option"></a>Opção JpegYCrCbSubsampling

Especifica a taxa de subampling a ser usada para codificação YCrCb.

O valor padrão é [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).

### <a name="suppressapp0-option"></a>Opção SuppressApp0

Especifica se a gravação de metadados do App0 deve ser suprimida durante a codificação dos dados da imagem.

O valor padrão é **FALSE**.

## <a name="decoding"></a>Decodificação

A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

O codec jpeg nativo também dá suporte ao [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na decodificação de quadro adicionando opções de suporte para decodificar um fluxo de imagem. Para obter mais informações sobre essas opções avançadas, consulte Visão geral das [fontes de bitmap.](-wic-bitmapsources.md)

 

 
