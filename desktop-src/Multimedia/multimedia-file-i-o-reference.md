---
title: Referência de e/s de arquivo de multimídia
description: Referência de e/s de arquivo de multimídia
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows multimídia, referência de e/s de arquivo
- multimídia, referência de e/s de arquivo
- entrada de multimídia, referência de e/s de arquivo
- referência de e/s de arquivo de multimídia
- e/s de arquivo, referência
- entrada e saída (e/s), referência
- E/s (entrada e saída), referência
- referência para e/s de arquivo de multimídia, sobre
- referência de e/s de arquivo de multimídia, sobre
- referência de e/s de arquivo, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d61b06c16b12a9276adc0d858a3170dae2f7d636cc63a9ac6cc032a65c978c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136897"
---
# <a name="multimedia-file-io-reference"></a>Referência de e/s de arquivo de multimídia

Esta seção descreve as funções, macros, mensagens e estruturas associadas à saída e entrada de arquivo multimídia. Esses elementos são agrupados da seguinte maneira.

## <a name="basic-io"></a>E/s básica

-   [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a>E/s em buffer

-   [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))
-   [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a>E/S DO RIFF

-   [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a>Procedimentos de e/s personalizados

-   [**IOProc**](/previous-versions//dd757098(v=vs.85))
-   [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [**MMIOM \_ fechar**](mmiom-close.md)
-   [**MMIOM \_ abrir**](mmiom-open.md)
-   [**MMIOM \_ leitura**](mmiom-read.md)
-   [**\_renomear MMIOM**](mmiom-rename.md)
-   [**MMIOM \_ Seek**](mmiom-seek.md)
-   [**MMIOM \_ gravação**](mmiom-write.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)
-   [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[E/s de arquivo multimídia](multimedia-file-i-o.md)
</dt> </dl>

 

 