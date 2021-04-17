---
description: Especifica se um decodificador AAC usa equações de downmix estéreo MPEG-2/MPEG-4 ou usa um downmix não padrão.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Propriedade AVDecAACDownmixMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105757901"
---
# <a name="avdecaacdownmixmode-property"></a>Propriedade AVDecAACDownmixMode

Especifica se um decodificador AAC usa equações de downmix estéreo MPEG-2/MPEG-4 ou usa um downmix não padrão.

Um exemplo de um downmix não padrão é o definido por ARIB do documento STD-B21 versão 4,4.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecAACDownmixMode**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um membro da enumeração [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

