---
description: Interrompe a passagem de codificação atual ou consulta se a passagem de codificação atual é a última.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propriedade AVEncCommonPassEnd (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02faeb9d78f10b962b7134fd316bda348b0f03e1a82ace210956c2243231df19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873366"
---
# <a name="avenccommonpassend-property"></a>Propriedade AVEncCommonPassEnd

Interrompe a passagem de codificação atual ou consulta se a passagem de codificação atual é a última.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Comentários

Definir essa propriedade como **VARIANT \_ TRUE** encerra a passagem de codificação atual. Definir essa propriedade como **VARIANT \_ FALSE** encerra a codificação multipass.

Ler essa propriedade consulta se a passagem de codificação atual é a última.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




