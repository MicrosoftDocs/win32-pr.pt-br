---
description: Especifica o modo de controle de intervalo dinâmico que será usado pelo decodificador de áudio.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: Propriedade MFPKEY_WMADEC_DRCMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164922"
---
# <a name="mfpkey_wmadec_drcmode-property"></a>\_Propriedade MFPKEY WMADEC \_ DRCMODE

Especifica o modo de controle de intervalo dinâmico que será usado pelo decodificador de áudio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACDRCSetting

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

Esse valor inteiro varia de 0 a 2. Quanto maior o valor, menor o intervalo dinâmico da saída de áudio descompactado. Um valor de 0 sinaliza o codec para não executar nenhum controle de intervalo dinâmico, ou seja, o codec não alterará o intervalo dinâmico inerente do conteúdo codificado.

Se esse valor for definido como 1 ou 2, o codec usará as seguintes propriedades para determinar o controle de intervalo dinâmico necessário:

-   [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)
-   [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)

Se você não fornecer valores de destino, o codec fornecerá seu próprio.

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

 

 




