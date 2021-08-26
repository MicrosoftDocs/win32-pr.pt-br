---
description: Especifica se o decodificador cai intra frames com quadros de referência ausentes.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Propriedade AVDecVideoDropPicWithMissingRef (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac5e8c02c63c977d8d5a8e47bb5d6f878c538364ac2fe5b65c1e691c84ca23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000316"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>Propriedade AVDecVideoDropPicWithMissingRef

Especifica se o decodificador cai intra frames com quadros de referência ausentes.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoDropPicWithMissingRef**

## <a name="remarks"></a>Comentários

Se o fragmentado estiver corrompido, um quadro poderá ter quadros de referência ausentes. Se o valor dessa propriedade for **Variant \_ true**, o decodificador descartará o quadro. Se o valor for **Variant \_ false**, o decodificador tentará decodificar o quadro, usando um ou mais quadros próximos como quadros de referência. O quadro decodificado resultante terá artefatos de bloqueio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




