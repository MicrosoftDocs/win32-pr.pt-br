---
description: Define o identificador do SPS (conjunto de parâmetros de sequência) na unidade NAL (camada de abstração de rede) do fluxo H.264 bits.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da06e431a3747e676e3934ac9a261e1d0e1ec37e18bacf01f8a3e623c4257488
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664656"
---
# <a name="codecapi_avench264spsid-property"></a>Propriedade CODECAPI \_ AVEncH264SPSID

Define o identificador do SPS (conjunto de parâmetros de sequência) na unidade NAL (camada de abstração de rede) do fluxo H.264 bits.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncH264SPSID**

## <a name="property-value"></a>Valor da propriedade

Especifica o valor da **\_ \_ \_ ID do** conjunto de parâmetros seq na unidade SPS NAL. O **elemento de sintaxe de \_ \_ \_ ID do** conjunto de parâmetros seq identifica o conjunto de parâmetros de sequência. O fluxo de bits resultante pode ser concatenado com outros fluxos de bits para produzir um fluxo de bits mais longo que contém vários conjuntos de parâmetros de sequência com diferentes identificadores SPS.

O intervalo válido é 0 31, conforme especificado na especificação H.264/AVC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

