---
description: Desabilita a conversão de taxa de quadros na MFT do processador de vídeo.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Atributo MF_XVP_DISABLE_FRC (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e82c60438a91111ffce6cc80c71fa76231b8e00d85644f4f56f1b496202d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940326"
---
# <a name="mf_xvp_disable_frc-attribute"></a>MF \_ XVP \_ desabilitar o \_ atributo FRC

Desabilita a conversão de taxa de quadros na [**MFT do processador de vídeo**](video-processor-mft.md).

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, o processador de vídeo não executará a conversão de taxa de quadros. Por padrão, o processador de vídeo converterá a taxa de quadros para corresponder ao tipo de mídia de saída.

Para definir este atributo:

1.  Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no processador de vídeo.
2.  Chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Defina o atributo antes de o streaming começar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




