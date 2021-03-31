---
description: Especifica se o codificador usa a codificação de taxa de bits variável (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: Propriedade MFPKEY_VBRENABLED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827894"
---
# <a name="mfpkey_vbrenabled-property"></a>\_Propriedade MFPKEY VBRENABLED

Especifica se o codificador usa a codificação de taxa de bits variável (VBR). Leitura/gravação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ falso**

## <a name="remarks"></a>Comentários

Esse valor deve ser definido como **Variant \_ true** para qualquer uma das outras propriedades de VBR a ser usada pelo codec.

Depois de definir esse valor como **Variant \_ true** no codificador de áudio, os tipos de saída recuperados usando o método [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) são tipos de VBR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MFPKEY \_ restringir \_ VBRQUALITY enumerado \_**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
