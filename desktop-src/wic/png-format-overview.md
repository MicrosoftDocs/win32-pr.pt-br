---
description: Este tópico fornece informações sobre o codec PNG nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Visão geral do formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444437"
---
# <a name="png-format-overview"></a>Visão geral do formato PNG

Este tópico fornece informações sobre o codec PNG nativo disponível por meio do Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidade do codec

A tabela a seguir fornece informações de identificação do codec.



|     Componente          | Descrição                     |
|------------------------|---------------------------------|
| Nome (s) formal (es)         | PNG |
| Extensão (s) de nome de arquivo | png                             |
| tipo MIME              | image/png                       |
| Suporte à especificação  | Especificação de PNG 1,2           |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes do codec PNG nativo.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | \_CONTAINERFORMATPNG GUID | 1b7cfaf4-713f-473c-bbcd6137425faeaf |
| Decodificador          | \_WICPNGDECODER CLSID     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Codificador          | \_WICPNGENCODER CLSID     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 e posterior

A partir do WIC do Windows 8 fornece um decodificador PNG adicional

## <a name="encoding"></a>Codificação

A API de codificação do WIC é projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre codificação de imagem usando a API do WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções de codificador

Os codecs habilitados para WIC diferem no nível de opção de codificação. As opções de codificador refletem os recursos de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas compatíveis com o WIC disponíveis para todos os códigos habilitados para WIC (embora não sejam necessariamente suportados) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte [visão geral da codificação](-wic-creating-encoder.md).

O codec PNG usa opções básicas de codificador de WIC. A tabela a seguir lista as opções de codificador do WIC compatíveis com o codec PNG nativo.



| Nome da propriedade   | VARTYPE  | Intervalo de valores                                                 | Valor Padrão                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | BOOL do VT \_ | **Verdadeiro** / **Falso**                                          | **FALSE**                                                        |
| FilterOption    | \_UI1 VT  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Se uma opção de codificador estiver presente na lista de opções de [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) para a qual o codec não dá suporte, ela será ignorada.

### <a name="interlaceoption"></a>InterlaceOption

Especifica se os dados da imagem devem ser codificados como entrelaçados.

O valor padrão é **FALSE**.

### <a name="filteroption"></a>FilterOption

Especifica a opção de filtro a ser usada para compactação de imagem.

O valor padrão é [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).

## <a name="decoding"></a>Decodificação

A API de decodificação de WIC é projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a decodificação de imagem, consulte a [visão geral da decodificação](-wic-creating-decoder.md). Para obter mais informações sobre como usar dados de imagem decodificados, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

O codec PNG nativo também dá suporte ao [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na decodificação de quadros adicionando opções avançadas para decodificar um fluxo de imagem. Para obter mais informações sobre essas opções avançadas, consulte a [visão geral de fontes de bitmap](-wic-bitmapsources.md).

 

 
