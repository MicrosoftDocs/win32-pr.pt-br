---
description: Especifica se uma transformação Media Foundation (MFT) dá suporte a vídeo estéreo 3D.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: MFT_SUPPORT_3DVIDEO atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da60bac92d1274f9d9a6624e247fc24d122ec26eabc103ad2d43477ae8f6b64b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776986"
---
# <a name="mft_support_3dvideo-attribute"></a>Atributo \_ MFT SUPPORT \_ 3DVIDEO

Especifica se uma transformação Media Foundation (MFT) dá suporte a vídeo estéreo 3D.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Para consultar esse atributo, chame [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o armazenamento de atributo global do MFT. Se **GetAttributes for** bem-sucedido, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

O valor padrão desse atributo é **FALSE.** Trate esse atributo como somente leitura. Não altere o valor; O MFT ignorará as alterações no valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




