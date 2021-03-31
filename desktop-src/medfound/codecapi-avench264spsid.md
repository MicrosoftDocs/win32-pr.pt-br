---
description: Define o identificador do conjunto de parâmetros de sequência (SPS) na unidade da NAL (camada de abstração de rede) do SPS do fluxo de bits H. 264.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: Propriedade CODECAPI_AVEncH264SPSID (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089787"
---
# <a name="codecapi_avench264spsid-property"></a>\_Propriedade CODECAPI AVEncH264SPSID

Define o identificador do conjunto de parâmetros de sequência (SPS) na unidade da NAL (camada de abstração de rede) do SPS do fluxo de bits H. 264.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncH264SPSID**

## <a name="property-value"></a>Valor da propriedade

Especifica o valor da **\_ ID do \_ conjunto \_ de parâmetros Seq** na unidade de nal do SPS. O elemento sintaxe de **\_ ID do \_ conjunto \_ de parâmetros Seq** identifica o conjunto de parâmetros de sequência. O fluxo de bits resultante pode ser concatenado com outros fluxos de bits, para produzir um fluxo de bits mais longo que contenha vários conjuntos de parâmetros de sequência com diferentes identificadores de SPS.

O intervalo válido é de 0 31, conforme especificado na especificação H. 264/AVC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

