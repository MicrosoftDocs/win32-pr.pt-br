---
description: Especifica se o aplicativo requer desempenho de codificação em tempo real.
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: Propriedade AVEncCommonRealTime (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b718f4f58d230448689700fc2e681c109e645d48cb33eb1788e45ac607350951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403886"
---
# <a name="avenccommonrealtime-property"></a>Propriedade AVEncCommonRealTime

Especifica se o aplicativo requer desempenho de codificação em tempo real.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonRealTime**

## <a name="remarks"></a>Comentários

Para especificar que a codificação deve ser executada em tempo real, de definir essa propriedade como **VARIANT \_ TRUE.** Codecs também podem retornar essa propriedade como uma funcionalidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




