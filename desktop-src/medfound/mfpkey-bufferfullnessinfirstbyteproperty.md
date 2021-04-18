---
description: Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: Propriedade MFPKEY_BUFFERFULLNESSINFIRSTBYTE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796125"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>\_Propriedade MFPKEY BUFFERFULLNESSINFIRSTBYTE

Especifica se o fluxo de bits de vídeo codificado contém um valor de total de buffer com cada quadro-chave.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="remarks"></a>Comentários

Você deve definir um tipo de saída antes de obter esse valor.

Você pode obter o valor dessa propriedade usando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Se você usar **IPropertyBag**, deverá primeiro definir o valor FOURCC do formato compactado desejado com a propriedade [ \_ FOURCC MFPKEY](mfpkey-fourccproperty.md) .

Ter a totalidade do buffer no primeiro byte de todos os quadros-chave permite que você determine o tamanho do buffer necessário ao concatenar fluxos de vídeo compactados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




