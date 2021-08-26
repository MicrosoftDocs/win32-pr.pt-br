---
description: Especifica a média de bytes por segundo em um fluxo de áudio de taxa de bits de variável (VBR) com base em qualidade.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: Propriedade MFPKEY_WMAENC_AVGBYTESPERSEC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfadc41e9f2c9f4410bc84c6d8bf23f30c559b96c83abba80beb719e8ccb8eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953296"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>\_Propriedade MFPKEY WMAENC \_ AVGBYTESPERSEC

Especifica a média de bytes por segundo em um fluxo de áudio de taxa de bits de variável (VBR) com base em qualidade.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACAvgBytesPerSecond

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Você pode obter esse valor do decodificador depois que o fluxo é codificado.

Esse valor é exigido pelo decodificador de áudio para descompactar corretamente o conteúdo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




