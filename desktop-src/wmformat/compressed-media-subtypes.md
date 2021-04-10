---
title: Subtipos de mídia compactados
description: Subtipos de mídia compactados
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- SDK do Windows Media Format, tipos de mídia
- ASF (Advanced Systems Format), tipos de mídia
- ASF (formato de sistemas avançados), tipos de mídia
- SDK do Windows Media Format, subtipos de mídia compactados
- Formato de sistema avançado (ASF), subtipos de mídia compactados
- ASF (formato de sistemas avançados), subtipos de mídia compactados
- tipos de mídia, subtipos de mídia compactados
- subtipos de mídia compactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d92d192d04257f0375a618dda05aa97fd3f344b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084045"
---
# <a name="compressed-media-subtypes"></a>Subtipos de mídia compactados

A tabela a seguir lista os subtipos de mídia compactados. Esses tipos são usados para identificar fluxos compactados em um arquivo. Ao configurar um fluxo de vídeo ou áudio, geralmente você usará esses tipos.



| Subtipo de mídia compactada          | Descrição                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | Áudio codificado com o codec Sipro Labs ACELP. Esse áudio normalmente é de dados de voz. (Não há mais suporte para codificação.)                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ MP43              | Vídeo codificado pelo Microsoft MPEG 4 codec versão 3. Esse codec não é mais suportado pelo Windows Media Format SDK. Se esse codec já estiver instalado em um computador, instalar o Windows Media Format SDK ou o pacote de redistribuição em um computador não removerá esse codec. |
| WMMEDIASUBTYPE \_ MP4S              | Vídeo codificado usando o codec ISO MPEG 4 versão 1.                                                                                                                                                                                                                                         |
| Vídeo do WMMEDIASUBTYPE \_ MPEG2 \_      | Vídeo codificado para especificações MPEG 2.                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | Vídeo codificado com o codec de tela do Windows Media versão 1.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | Vídeo codificado com o codec de tela do Windows Media Video 9.                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | Vídeo codificado com o codec de imagem do Windows Media Video 9 para transformar bitmaps e dados de deformações em um fluxo de vídeo.                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | Vídeo codificado com o codec do Windows Media Video 9 Image v2.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | Áudio codificado com o codec Windows Media Audio 9 Lossless ou o codec Windows Media Audio 9,1.                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | Áudio codificado com o Windows Media Audio Codec versão 2. Esse valor é idêntico a WMMEDIASUBTYPE \_ WMAudioV7 e WMMEDIASUBTYPE \_ WMAudioV8, porque o fragmentado para essas versões de codec são compatíveis.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | Áudio codificado com o Windows Media Audio Codec versão 7. Esse valor é idêntico a WMMEDIASUBTYPE \_ WMAudioV2 e WMMEDIASUBTYPE \_ WMAudioV8, porque o fragmentado para essas versões de codec são compatíveis.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | Áudio codificado com o codec Windows Media Audio 8, o codec Windows Media Audio 9 ou o codec Windows Media Audio 9,1. Esse valor é idêntico a WMMEDIASUBTYPE \_ WMAudioV2 e WMMEDIASUBTYPE \_ WMAudioV7, porque o fragmentado para essas versões de codec são compatíveis.              |
| WMMEDIASUBTYPE \_ WMAudioV9         | Áudio codificado com o codec Windows Media Audio 9 Professional ou o codec Windows Media Audio 9,1 Professional.                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | Vídeo codificado com o codec ISO MPEG4 v 1.1.                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | Áudio codificado com o codec de voz do Windows Media Audio 9.                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | Vídeo codificado usando o Windows Media Video Codec versão 7.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMV2              | Vídeo codificado usando o codec Windows Media Video 8.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMV3              | Vídeo codificado usando o codec do Windows Media Video 9.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | Vídeo codificado usando a versão do codec de perfil avançado do vídeo do Windows Media 9 que foi lançado com o SDK da série Windows Media Format 9 Series.                                                                                                                                           |
| WMMEDIASUBTYPE \_ WVC1              | Vídeo codificado usando a versão do codec de perfil avançado do Windows Media Video 9 que foi lançado com o SDK do Windows Media Format 11. Esse subtipo identifica um fluxo de bits que é compatível com o padrão SMPTE VC-1.                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de tipo de mídia**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de mídia**](media-types.md)
</dt> <dt>

[**Subtipos de mídia descompactados**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




