---
description: Especifica o máximo de quadros de referência com suporte pelo codificador.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: CODECAPI_AVEncVideoMaxNumRefFrame propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e11e7325628f0e7c1e6560d3fc734b34e8a032a3fbf3630aa1fb5959cec33a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606416"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>Propriedade CODECAPI \_ AVEncVideoMaxNumRefFrame

Especifica o máximo de quadros de referência com suporte pelo codificador.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>Comentários

Para H.264, isso é mapeado para a variável conjunto de parâmetros de sequência **max \_ num ref \_ \_ frames** conforme definido na especificação H.264.

**Codificadores H.264/AVC:**

Os codificadores podem usar menos quadros de referência para obedecer ao nível especificado no bitstream.

Os codificadores devem dar [**suporte a GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRangee.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Essa é uma propriedade estática que significa que ela só pode ser definida antes do início da sessão de codificação.

O valor padrão recomendado é 2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

