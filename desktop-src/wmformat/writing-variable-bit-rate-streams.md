---
title: Gravando fluxos de taxa de bits variáveis
description: Gravando fluxos de taxa de bits variáveis
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- ASF (Advanced Systems Format), gravando fluxos de VBR
- ASF (formato de sistemas avançados), gravando fluxos de VBR
- taxa de bits variável (VBR), gravando fluxos
- VBR (taxa de bits variável), gravando fluxos
- fluxos, gravando VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640119"
---
# <a name="writing-variable-bit-rate-streams"></a>Gravando fluxos de taxa de bits variáveis

Os fluxos de taxa de bits variável (VBR) são gravados da mesma forma que os fluxos de taxa de bits constante (CBR). A única diferença está no processamento realizado internamente pelo gravador e pelos codecs. No entanto, a taxa de bits (restrita e irrestrita) baseada em taxas de bit requer uma passagem de pré-processamento no gravador.

Você deve verificar o valor de retorno para a primeira chamada feita para [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) para cada fluxo. Se o código de erro retornado for \_ um número inválido de e/s do NS \_ \_ \_ , o fluxo exigirá uma passagem de pré-processamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando a codificação Two-Pass**](using-two-pass-encoding.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




