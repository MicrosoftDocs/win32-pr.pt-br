---
description: Este tópico fornece informações sobre o codec BMP nativo disponível por meio do WIC (Windows Imaging Component).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Visão geral do formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975f27af5b731ed1f62f3571109553848705239
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444957"
---
# <a name="bmp-format-overview"></a>Visão geral do formato BMP

Este tópico fornece informações sobre o codec BMP nativo disponível por meio do WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identidade do Codec

A tabela a seguir fornece informações de identificação de codec.



| Componente              | Descrição           |
|------------------------|-----------------------|
| Nomes formais         | Formato bitmap do Windows |
| Extensões de nome de arquivo | bmp, dib              |
| tipo MIME              | image/bmp             |
| Suporte à especificação  | Especificação BMP v5  |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes nativos do codec BMP.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | Contêiner \_ GUIDFormatBmp | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| Decodificador          | CLSID \_ WICBmpDecoder     | 6b462062-7cbf-400d-9fdb813dd10f2778 |
| Codificador          | CLSID \_ WICBmpEncoder     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Codificação

A API de codificação WIC foi projetada para ser independente de codec e, portanto, a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções do codificador

Os codecs habilitados para WIC diferem no nível da opção de codificação. As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte Visão [geral da codificação](-wic-creating-encoder.md).

A tabela a seguir lista as opções do codificador WIC com suporte pelo codec BMP nativo.



| Nome da propriedade               | Vartype      | Intervalo de valores                      | Valor Padrão      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **BOOL da VT \_** | **VARIANT \_ TRUE/VARIANT \_ FALSE** | **VARIANT \_ FALSE** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Especifica se é necessário permitir a codificação de dados no formato de \_ pixel WICPixelFormat32bppBGRA de GUID. Se essa opção for definida como **VARIANT \_ TRUE,** o BMP será gravado com um header BITMAPV5HEADER.

O valor padrão é **VARIANT \_ FALSE.**

Se uma opção de codificador estiver presente na lista de opções IPropertyBag2 à qual o codec não dá suporte, ela será ignorada.

Observação para arquivos BMP do Windows de 16 bits e 32 bits, o codec BMP ignora qualquer canal alfa, pois muitos arquivos de imagem herdados contêm dados inválidos nesse canal extra. A partir do Windows 8, os arquivos BMP do Windows de 32 bits gravados usando **o BITMAPV5HEADER** com conteúdo de canal alfa válido são lidos como WICPixelFormat32bppBGRA

## <a name="decoding"></a>Decodificação

A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

 

 
