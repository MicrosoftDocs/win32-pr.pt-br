---
description: Desabilita a conversão de taxa de quadros na MFT do processador de vídeo.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Atributo MF_XVP_DISABLE_FRC (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921123"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




