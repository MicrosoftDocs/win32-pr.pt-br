---
description: Especifica a configuração padrão para o bit original no fluxo de áudio MPEG-1. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Propriedade AVEncMPAOriginalBitstream (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d39b34339e25d08b138fd1c55a64e8a84d6cf4b4db302cbab1e5f50b8ccebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689736"
---
# <a name="avencmpaoriginalbitstream-property"></a>Propriedade AVEncMPAOriginalBitstream

Especifica a configuração padrão para o bit original no fluxo de áudio MPEG-1. Essa propriedade se aplica a codificadores de áudio MPEG.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPAOriginalBitstream**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição          |
|----------------|----------------------|
| VARIANT \_ FALSE | O bit original está desligado. |
| VARIANT \_ TRUE  | O bit original está em.  |



 

## <a name="remarks"></a>Comentários

O codificador pode substituir essa configuração, com base no conteúdo do fluxo de entrada.

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

 

 




