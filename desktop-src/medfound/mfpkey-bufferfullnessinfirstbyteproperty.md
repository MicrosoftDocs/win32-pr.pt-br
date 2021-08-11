---
description: Especifica se o fluxo de bits de vídeo codificado contém um valor de fullness do buffer com cada quadro-chave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 087b505680dfc3c51fe2cb50cdae76a425ca2ff5798356e9893794d47a7e22e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242995"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>Propriedade MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE

Especifica se o fluxo de bits de vídeo codificado contém um valor de fullness do buffer com cada quadro-chave.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>Tipo de Dados

BOOL da VT \_

## <a name="remarks"></a>Comentários

Você deve definir um tipo de saída antes de obter esse valor.

Você pode obter o valor dessa propriedade usando [IWMCodecProps::GetCodecProp.](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) Se você usar **IPropertyBag**, deverá primeiro definir o valor FOURCC do formato compactado desejado com a [propriedade MFPKEY \_ FOURCC.](mfpkey-fourccproperty.md)

Ter a totalidade do buffer no primeiro byte de todos os quadros-chave permite determinar o tamanho do buffer necessário ao concatenar fluxos de vídeo compactados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




