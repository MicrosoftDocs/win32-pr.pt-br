---
description: Esse atributo especifica proteção adicional oferecida por uma OTA (autoridade de confiança de saída) de vídeo quando um conector não oferece proteção de saída.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Atributo MFPROTECTION_CONSTRICTVIDEO_NOOPM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d1d7cd858ec9cf254cca1dffc5fef4e24fbb5a3a288975a9f70c9ae118dde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713736"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>\_Atributo MFPROTECTION CONSTRICTVIDEO \_ NOOPM

Esse atributo especifica proteção adicional oferecida por uma OTA (autoridade de confiança de saída) de vídeo quando um conector não oferece proteção de saída.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Essa é uma proteção adicional oferecida por uma OTA (autoridade de confiança de saída) de vídeo quando um conector não oferece proteção de saída (consulte [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)). Nesse caso, o OTA pode oferecer essa proteção cujo efeito é o mesmo que a proteção [MFPROTECTION \_ CONSTRICTVIDEO](mfprotection-constrictvideo.md) . Isso é definido para evitar confusão com chamadas anteriores a [**IMFOutputPolicy:: GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) interações em que a presença da proteção do MFPROTECTION \_ CONSTRICTVIDEO foi usada para ajudar a identificar o pseudodispositivo do Gerenciador de janelas da área de trabalho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




