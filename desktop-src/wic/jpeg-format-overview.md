---
description: este tópico fornece informações sobre o codec JPEG nativo disponível por meio do Windows o componente de geração de imagens (WIC).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Visão geral do formato JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81f735f2ff13b7f5a36b71a73ebbac8fbfeceb62d6740477a8b741d43d46805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667046"
---
# <a name="jpeg-format-overview"></a>Visão geral do formato JPEG

este tópico fornece informações sobre o codec JPEG nativo disponível por meio do Windows o componente de geração de imagens (WIC).

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|   Componente            | Descrição                             |
|------------------------|-----------------------------------------|
| Nome (s) formal (es)         | JPEG |
| Extensão (s) de nome de arquivo | JPE, JPEG, jpg                          |
| tipo MIME              | imagem/JPEG, imagem/JPE, imagem/jpg        |
| Suporte à especificação  | Especificação JFIF 1, 2                 |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes do codec JPEG nativo.



| Componente        | Nome amigável             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATJPEG GUID | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Decodificador          | \_WICJPEGDECODER CLSID     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Codificador          | \_WICJPEGENCODER CLSID     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Codificação

A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções de codificador

Os codecs habilitados para WIC diferem no nível de opção de codificação. As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

O codec JPEG usa opções básicas de WIC. A tabela a seguir lista as opções de codificador do WIC compatíveis com o codec JPEG nativo.



| Nome da Propriedade                                        | VARTYPE           | Intervalo de valores                                                                       | Valor padrão                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0-1,0                                                                           | 0,9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | \_UI1 VT           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Luminância](#luminance-option)                       | \_Matriz VT UI4/VT \_ | 64 entradas (DCT)                                                                  | Tabela de luminância padrão.                                                       |
| [Crominância](#chrominance-option)                   | \_Matriz VT UI4/VT \_ | 64 entradas (DCT)                                                                  | Tabela crominância padrão.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | \_UI1 VT           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | BOOL do VT \_          | **Verdadeiro** / **Falso**                                                                | **FALSE**                                                                      |



 

Se uma opção de codificador estiver presente na lista de opções de [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) para a qual o codec não dá suporte, ela será ignorada.

### <a name="imagequality-option"></a>Opção ImageQuality

Especifica a fidelidade da imagem desejada. 0,0 indica a menor fidelidade possível e 1,0 especifica a fidelidade mais alta.

O valor padrão é 0,9.

### <a name="bitmaptransform-option"></a>Opção BitmapTransform

Especifica como a imagem deve ser transformada durante a decodificação de imagem. Essa opção deve ser definida como um dos valores de enumeração [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

O valor padrão é [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="luminance-option"></a>Opção de luminância

Especifica a tabela de nível de brilho em escala de cinza a ser usada para codificação.

### <a name="chrominance-option"></a>Opção crominância

Especifica a tabela crominância a ser usada para codificação.

### <a name="jpegycrcbsubsampling-option"></a>Opção JpegYCrCbSubsampling

Especifica a taxa de subamostração a ser usada para codificação YCrCb.

O valor padrão é [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).

### <a name="suppressapp0-option"></a>Opção SuppressApp0

Especifica se é para suprimir a gravação de metadados do App0 durante a codificação dos dados da imagem.

O valor padrão é **FALSE**.

## <a name="decoding"></a>Decodificação

A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md). Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

O codec JPEG nativo também dá suporte ao [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na decodificação de quadros adicionando opções avançada para decodificar um fluxo de imagem. Para obter mais informações sobre essas opções avançadas, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

 

 
