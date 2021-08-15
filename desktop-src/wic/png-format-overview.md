---
description: Este tópico fornece informações sobre o codec PNG nativo disponível por meio do WIC (Windows Imaging Component).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Visão geral do formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3d74282f8c14fd94b3661430402a808b04ceb9cf0a061a1648f7a912af5636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086749"
---
# <a name="png-format-overview"></a>Visão geral do formato PNG

Este tópico fornece informações sobre o codec PNG nativo disponível por meio do WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identidade do Codec

A tabela a seguir fornece informações de identificação de codec.



|     Componente          | Descrição                     |
|------------------------|---------------------------------|
| Nomes formais         | PNG |
| Extensões de nome de arquivo | png                             |
| tipo MIME              | image/png                       |
| Suporte à especificação  | Especificação PNG 1.2           |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec PNG.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | Contêiner \_ GUIDFormatPng | 1b7cfaf4-713f-473c-ltd6137425faeaf |
| Decodificador          | CLSID \_ WICPngDecoder     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Codificador          | CLSID \_ WICPngEncoder     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 e posterior

Começando com Windows 8 WIC fornece um decodificador PNG adicional

## <a name="encoding"></a>Codificação

A API de codificação WIC foi projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções do codificador

Os codecs habilitados para WIC diferem no nível da opção de codificação. As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte a Visão geral [de codificação](-wic-creating-encoder.md).

O codec PNG usa opções básicas do codificador WIC. A tabela a seguir lista as opções do codificador WIC com suporte pelo codec PNG nativo.



| Nome da Propriedade   | Vartype  | Intervalo de valores                                                 | Valor padrão                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | BOOL da VT \_ | **TRUE** / **FALSE**                                          | **FALSE**                                                        |
| FilterOption    | VT \_ UI1  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Se uma opção de codificador estiver presente na lista de opções [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) à qual o codec não dá suporte, ela será ignorada.

### <a name="interlaceoption"></a>InterlaceOption

Especifica se os dados da imagem serão codificados como entrelaçados.

O valor padrão é **FALSE**.

### <a name="filteroption"></a>FilterOption

Especifica a opção de filtro a ser usada para compactação de imagem.

O valor padrão é [**WICPngFilterUnspecified.**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption)

## <a name="decoding"></a>Decodificação

A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

O codec PNG nativo também dá suporte à [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) na decodificação de quadro adicionando opções avançadas para decodificar um fluxo de imagem. Para obter mais informações sobre essas opções avançadas, consulte Visão geral das [fontes de bitmap.](-wic-bitmapsources.md)

 

 
