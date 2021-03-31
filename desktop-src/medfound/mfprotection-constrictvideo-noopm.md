---
description: Esse atributo especifica proteção adicional oferecida por uma OTA (autoridade de confiança de saída) de vídeo quando um conector não oferece proteção de saída.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: Atributo MFPROTECTION_CONSTRICTVIDEO_NOOPM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921222"
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
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




