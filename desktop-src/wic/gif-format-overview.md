---
description: Este tópico fornece informações sobre o codec GIF nativo disponível por meio do Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Visão geral do formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf7e9924c921b7944de114f5fe667cb2aa33cae
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444447"
---
# <a name="gif-format-overview"></a>Visão geral do formato GIF

Este tópico fornece informações sobre o codec GIF nativo disponível por meio do Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidade do Codec

A tabela a seguir fornece informações de identificação de codec.



|  Componente             | Descrição                           |
|------------------------|---------------------------------------|
| Nomes formais         | Graphics Interchange Format 89a (GIF) |
| Extensões de nome de arquivo | GIF                                   |
| tipo MIME              | image/gif                             |
| Suporte à especificação  | Especificação GIF 89a/89m             |



 

A tabela a seguir lista os GUIDs usados para identificar os componentes nativos de codec gif.



| Componente        | Nome amigável            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato do contêiner | Contêiner \_ GUIDFormatGif | 1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5 |
| Decodificador          | CLSID \_ WICGifDecoder     | 381dda3c-9ce9-4834-a23e1f98f8fc52be |
| Codificador          | CLSID \_ WICGifEncoder     | 114f5598-0b22-40a0-86a1c83ea495adbd |



 

## <a name="encoding"></a>Codificação

A API de codificação WIC foi projetada para ser independente de codec e a codificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre a codificação de imagem usando a API WIC, consulte a [Visão geral de codificação](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Opções do codificador

Os codecs habilitados para WIC diferem no nível da opção de codificação. As opções do codificador refletem as funcionalidades de um codificador de imagem e cada codec nativo dá suporte a um conjunto dessas opções de codificador. As opções de codificador podem ser opções básicas com suporte do WIC disponíveis para todos os códigos habilitados para WIC (embora não necessariamente com suporte) ou opções específicas de codec projetadas pelo codec de formato de imagem. Para gerenciar essas opções de codificação durante o processo de codificação, o WIC usa a interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obter mais informações sobre como usar a interface **IPropertyBag2** para codificação WIC, consulte a Visão geral [de codificação](-wic-creating-encoder.md).

O codificador GIF não dá suporte a nenhuma opção básica do WIC e não fornece opções de codificador personalizadas. Se uma opção de codificador estiver na [**lista de opções IPropertyBag2,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) ela será ignorada.

## <a name="decoding"></a>Decodificação

A API de decodificação do WIC foi projetada para ser independente de codec e a decodificação de imagem para codecs habilitados para WIC é essencialmente a mesma. Para obter mais informações sobre decodificação de imagem, consulte Visão [geral de decodificação.](-wic-creating-decoder.md) Para obter mais informações sobre como usar dados de imagem decodificados, consulte Visão geral das [fontes de bitmap](-wic-bitmapsources.md).

 

 
