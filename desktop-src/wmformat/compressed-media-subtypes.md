---
title: Subtipos de mídia compactado
description: Subtipos de mídia compactado
ms.assetid: 0ed6b4e8-6450-4484-90d6-efa2f9101782
keywords:
- Windows SDK de Formato de Mídia, tipos de mídia
- ASF (Advanced Systems Format), tipos de mídia
- ASF (Formato de Sistemas Avançados), tipos de mídia
- Windows SDK de Formato de Mídia, subtipos de mídia compactados
- ASF (Advanced Systems Format), subtipos de mídia compactado
- ASF (Formato de Sistemas Avançados), subtipos de mídia compactados
- tipos de mídia, subtipos de mídia compactados
- subtipos de mídia compactado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f231c9c8ff666c11d3fb3bf101dc3b43c1cd2ff90ca3a28ca1af0113fe8fccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548086"
---
# <a name="compressed-media-subtypes"></a>Subtipos de mídia compactado

A tabela a seguir lista os subtipos de mídia compactados. Esses tipos são usados para identificar fluxos compactados em um arquivo. Ao configurar um fluxo de áudio ou vídeo, normalmente você usará esses tipos.



| Subtipo de mídia compactada          | Descrição                                                                                                                                                                                                                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ ACELPnet          | Áudio codificado com o codec ACELP do Sipro Labs. Esse áudio normalmente são dados de voz. (Não há mais suporte para codificação.)                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ MP43              | Vídeo codificado pelo codec do Microsoft MPEG 4 versão 3. Esse codec não é mais suportado pelo SDK Windows Formato de Mídia. Se esse codec já estiver instalado em um computador, instalar o SDK Windows Formato de Mídia ou o pacote de redistribuição em um computador não removerá esse codec. |
| WMMEDIASUBTYPE \_ MP4S              | Vídeo codificado usando o codec ISO MPEG 4 versão 1.                                                                                                                                                                                                                                         |
| VÍDEO DO WMMEDIASUBTYPE \_ MPEG2 \_      | Vídeo codificado para especificações do MPEG 2.                                                                                                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ MSS1              | Vídeo codificado com o codec Windows Media Screen versão 1.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ MSS2              | Vídeo codificado com o codec Windows Media Video 9.                                                                                                                                                                                                                                  |
| WMMEDIASUBTYPE \_ WMVP              | Vídeo codificado com o codec Windows Media Video 9 para transformar bitmaps e dados de deformação em um fluxo de vídeo.                                                                                                                                                                     |
| WMMEDIASUBTYPE \_ WVP2              | Vídeo codificado com o codec Windows Media Video 9 v2.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMAudio \_ Lossless | Áudio codificado com o codec Windows Media Audio 9 sem perda ou o codec Windows Media Audio 9.1.                                                                                                                                                                                           |
| WMMEDIASUBTYPE \_ WMAudioV2         | Áudio codificado com o codec Windows Media Audio codec versão 2. Esse valor é idêntico ao WMMEDIASUBTYPE \_ WMAudioV7 e WMMEDIASUBTYPE WMAudioV8, porque os bitstreams para essas versões \_ de codec são compatíveis.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV7         | Áudio codificado com o codec Windows Media Audio codec versão 7. Esse valor é idêntico ao WMMEDIASUBTYPE \_ WMAudioV2 e WMMEDIASUBTYPE WMAudioV8, porque os bitstreams para essas \_ versões de codec são compatíveis.                                                                             |
| WMMEDIASUBTYPE \_ WMAudioV8         | Áudio codificado com o codec Windows Media Audio 8, o codec Windows Media Audio 9 ou o codec Windows Media Audio 9.1. Esse valor é idêntico a WMMEDIASUBTYPE \_ WMAudioV2 e WMMEDIASUBTYPE WMAudioV7, porque os bitstreams para essas versões \_ de codec são compatíveis.              |
| WMMEDIASUBTYPE \_ WMAudioV9         | Áudio codificado com o codec Windows Media Audio 9 Professional ou o codec Windows Media Audio 9.1 Professional.                                                                                                                                                                          |
| WMMEDIASUBTYPE \_ M4S2              | Vídeo codificado com o codec ISO MPEG4 v1.1.                                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMSP1             | Áudio codificado com o codec Windows Media Audio 9 Voice.                                                                                                                                                                                                                                   |
| WMMEDIASUBTYPE \_ WMV1              | Vídeo codificado usando o codec Windows Media Video codec versão 7.                                                                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ WMV2              | Vídeo codificado usando o codec Windows Media Video 8.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMV3              | Vídeo codificado usando o codec Windows Media Video 9.                                                                                                                                                                                                                                        |
| WMMEDIASUBTYPE \_ WMVA              | Vídeo codificado usando a versão do codec Windows Media Video 9 Advanced Profile que foi lançado com o SDK Windows Media Format 9 Series.                                                                                                                                           |
| WMMEDIASUBTYPE \_ WVC1              | Vídeo codificado usando a versão do codec Windows Media Video 9 Advanced Profile que foi lançado com o SDK Windows Media Format 11. Esse subtipo identifica um fluxo de bits compatível com o padrão VC-1 do SMPTE.                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de tipo de mídia**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de mídia**](media-types.md)
</dt> <dt>

[**Subtipos de mídia descompactados**](uncompressed-media-subtypes.md)
</dt> </dl>

 

 




