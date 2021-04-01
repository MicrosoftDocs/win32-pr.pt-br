---
description: Especifica o número máximo de quadros de referência com suporte no codificador.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Propriedade CODECAPI_AVEncVideoMaxNumRefFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104091877"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>\_Propriedade CODECAPI AVEncVideoMaxNumRefFrame

Especifica o número máximo de quadros de referência com suporte no codificador.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>Comentários

Para H. 264, isso é mapeado para a variável de conjunto de parâmetros de sequência **Max \_ num \_ ref \_ frames** , conforme definido na especificação H. 264.

**Codificadores H. 264/AVC:**

Os codificadores podem usar menos quadros de referência para obedecer ao nível especificado no fragmentado.

Os codificadores devem dar suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Essa é uma propriedade estática, o que significa que ela só pode ser definida antes do início da sessão de codificação.

O valor padrão recomendado é 2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

