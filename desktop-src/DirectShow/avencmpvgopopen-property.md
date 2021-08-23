---
description: Especifica se o codificador produz goPs (grupos abertos de imagens) ou GOPs fechados. Essa propriedade se aplica a codificadores de vídeo MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Propriedade AVEncMPVGOPOpen (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6be085bde5588fecd5a2274d442f38d4198702475f3ed13c7bb3a5569687375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540896"
---
# <a name="avencmpvgopopen-property"></a>Propriedade AVEncMPVGOPOpen

Especifica se o codificador produz goPs (grupos abertos de imagens) ou GOPs fechados. Essa propriedade se aplica a codificadores de vídeo MPEG.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPVGOPOpen**

## <a name="property-value"></a>Valor da propriedade



| Valor          | Descrição |
|----------------|-------------|
| VARIANT \_ FALSE | GOPs fechados |
| VARIANT \_ TRUE  | Abrir GOPs   |



 

## <a name="remarks"></a>Comentários

Um GOP aberto contém quadros delta que referenciam quadros do GOP anterior. Um GOP fechado não contém quadros delta que referenciam o GOP anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional aplicativos \[ UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




