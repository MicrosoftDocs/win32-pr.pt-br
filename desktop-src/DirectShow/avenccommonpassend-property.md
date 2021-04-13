---
description: Interrompe a passagem de codificação atual ou consulta se a passagem de codificação atual é a última.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propriedade AVEncCommonPassEnd (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456823"
---
# <a name="avenccommonpassend-property"></a>Propriedade AVEncCommonPassEnd

Interrompe a passagem de codificação atual ou consulta se a passagem de codificação atual é a última.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Comentários

Definir essa propriedade como **Variant \_ true** finaliza a passagem de codificação atual. A definição dessa propriedade como **variante \_ false** encerra a codificação de passagem.

A leitura desta propriedade consulta se a passagem de codificação atual é a última.

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

 

 




