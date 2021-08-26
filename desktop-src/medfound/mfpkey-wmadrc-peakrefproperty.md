---
description: Especifica o nível de volume mais alto que ocorre no conteúdo de áudio.
ms.assetid: 177311c4-c348-4d38-8c8d-b6690643529c
title: MFPKEY_WMADRC_PEAKREF propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58013ba116b9217ad6c16c93e420a09872cd887c4d5068f7c5b5dd68bf013377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953446"
---
# <a name="mfpkey_wmadrc_peakref-property"></a>Propriedade MFPKEY \_ WMADRC \_ PEAKREF

Especifica o nível de volume mais alto que ocorre no conteúdo de áudio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCPeakReference

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="remarks"></a>Comentários

Você pode obter esse valor do codificador depois que o conteúdo for processado. Esse valor também pode ser definido no decodificador para controle de intervalo dinâmico.

Para obter mais informações sobre o controle de intervalo dinâmico, consulte o artigo da Web Windows Recursos do [Codec de Áudio Professional Mídia.](/previous-versions/ms867218(v=msdn.10))

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
