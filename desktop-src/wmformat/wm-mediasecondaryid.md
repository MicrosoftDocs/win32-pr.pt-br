---
title: WM/MediaClassSecondaryID
description: O atributo WM/MediaClassSecondaryID contém o GUID da classe de mídia secundária.
ms.assetid: 3d1429bc-f168-4b25-9d26-c1c28b852160
keywords:
- Formato de mídia do Windows WM/MediaClassSecondaryID
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a37c0b4314a518132d08454ef2cf7472273795cbb0b50f98d22b800e06cc1b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431640"
---
# <a name="wmmediaclasssecondaryid"></a>WM/MediaClassSecondaryID

O **atributo WM/MediaClassSecondaryID** contém o GUID da classe de mídia secundária.

## <a name="global-constant"></a>Constante global

g \_ wszWMMediaClassSecondaryID

## <a name="data-type"></a>Tipo de Dados

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

Esse atributo deve ser definido como um dos valores na tabela a seguir.



| GUID da classe secundária                   | Descrição                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "E0236BEB-C281-4EDE-A36D-7AF76A3D45B5" | Use para arquivos de audio book.                                                                                                                                                               |
| "3A172A13-2BD9-4831-835B-114F6A95943F" | Use para arquivos de áudio que contêm palavras faladas, mas não são livros de áudio. Por exemplo, rotinas de rotina em stand-up.                                                                           |
| "6677DB9B-E5A0-4063-A1AD-ACEB52840CF1" | Use para arquivos de áudio relacionados a notícias.                                                                                                                                                    |
| "1B824A67-3F80-4E3E-9CDE-F7361B0F5F1B" | Use para arquivos de áudio com conteúdo de talk show.                                                                                                                                             |
| "1FE2E091-4E1E-40CE-B22D-348C732E0B10" | Use para arquivos de vídeo relacionados a notícias.                                                                                                                                                    |
| "D6DE1D88-C77C-4593-BFBC-9C61E8C373E3" | Use para arquivos de vídeo que contêm programas baseados na Web, shorts, trailers de filme e assim por diante. Esse é o identificador geral para entretenimento em vídeo que não se ajusta a outra categoria. |
| "00033368-5009-4AC3-A820-5D2D09A4E7C1" | Use para arquivos de áudio que contêm clipes de som de jogos.                                                                                                                                  |
| "F24FF731-96FC-4D0F-A2F5-5A3483682B1A" | Use para arquivos de áudio que contêm músicas completas de faixas de som do jogo. Se apenas parte de uma música for codificada no arquivo, use o identificador para clipes de som do jogo.                   |
| "E3E689E2-BA8C-4330-96DF-A0EEEFFA6876" | Use para arquivos de vídeo que contêm vídeos de música.                                                                                                                                            |
| "B76628F4-300D-443D-9CB5-01C285109DAF" | Use para arquivos de vídeo que contêm vídeo em home geral.                                                                                                                                      |
| "A9B87FC9-BD47-4BF0-AC4F-655B89F7D868" | Use para arquivos de vídeo que contêm recursos.                                                                                                                                           |
| "BA7F258A-62F7-47A9-B21F-4651C42A000E" | Use para arquivos de vídeo que contêm programas de tv. Para programas baseados na Web, use o identificador mais genérico.                                                                                  |
| "44051B5B-B103-4B5C-92AB-93060A9463F0" | Use para arquivos de vídeo que contêm vídeo corporativo. Por exemplo, reuniões gravadas ou vídeos de treinamento.                                                                                      |
| "0B710218-8C0C-475E-AF73-4C41C0C8F8CE" | Use para arquivos de vídeo que contêm vídeo em casa feito de fotografias.                                                                                                                        |



 

Ao especificar um identificador de classe secundária, o arquivo também deve conter um atributo de identificador de classe primária.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)
</dt> </dl>

 

 




