---
title: Escrevendo a taxa de bits variável Fluxos
description: Escrevendo a taxa de bits variável Fluxos
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- ASF (Advanced Systems Format), escrevendo fluxos VBR
- ASF (Formato de Sistemas Avançados), escrevendo fluxos VBR
- taxa de bits variável (VBR), escrevendo fluxos
- VBR (taxa de bits variável), escrevendo fluxos
- streams, escrevendo VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694774613ada8b4be05eab55be3213898d423d3b6ac4438204d149a0bd606c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930247"
---
# <a name="writing-variable-bit-rate-streams"></a>Escrevendo a taxa de bits variável Fluxos

Os fluxos de taxa de bits variável (VBR) são gravados da mesma maneira que os fluxos CBR (taxa de bits constante). A única diferença está no processamento executado internamente pelo autor e pelos codecs. No entanto, a VBR baseada em taxa de bits (restrita e irr pouco restrita) requer uma passagem de pré-processamento no autor.

Você deve verificar o valor de retorno para a primeira chamada que fizer a [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) para cada fluxo. Se o código de erro retornado for NS \_ E \_ INVALID NUM \_ \_ PASSES, o fluxo exigirá uma passagem de pré-processamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando Two-Pass codificação**](using-two-pass-encoding.md)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




