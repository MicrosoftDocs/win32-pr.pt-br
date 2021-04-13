---
description: Especifica a configuração padrão para o bit de direitos autorais no fluxo de áudio MPEG-1. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Propriedade AVEncMPACopyright (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370270"
---
# <a name="avencmpacopyright-property"></a>Propriedade AVEncMPACopyright

Especifica a configuração padrão para o bit de direitos autorais no fluxo de áudio MPEG-1. Essa propriedade se aplica a codificadores de áudio MPEG.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPACopyright**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição           |
|----------------|-----------------------|
| VARIANTE \_ falso | O bit de Copyright está desativado. |
| VARIANTE \_ true  | O bit de Copyright está ativado.  |



 

## <a name="remarks"></a>Comentários

O codificador pode substituir essa configuração, com base no conteúdo do fluxo de entrada.

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

 

 




