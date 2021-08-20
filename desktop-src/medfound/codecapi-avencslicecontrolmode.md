---
description: Especifica o modo de controle de fatia. Os valores válidos são 0, 1 e 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: CODECAPI_AVEncSliceControlMode propriedade (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8ed749419533e4c8c4cec1e6f977bcfa8586c20d43d27d56a2dd041ab5b0267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064767"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>Propriedade CODECAPI \_ AVEncSliceControlMode

Especifica o modo de controle de fatia. Os valores válidos são 0, 1 e 2.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncSliceControlMode**

## <a name="property-value"></a>Valor da propriedade

Valores de modo de controle de fatia:



| Valor                                                                        | Significado                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Definir esse valor como 0 indica que a propriedade [ \_ CODECAPI AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de macroblocks por fatia.<br/>     |
| <dl> <dt>1</dt> </dl> | Definir esse valor como 1 indica que a propriedade [ \_ CODECAPI AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de bits por fatia.<br/>            |
| <dl> <dt>2</dt> </dl> | Definir esse valor como 2 indica que a propriedade [ \_ CODECAPI AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de linhas de macroblock por fatia.<br/> |



 

O codificador retorna os valores aos que ele dá suporte.

## <a name="remarks"></a>Comentários

**Codificadores H.264/AVC:**

É recomendável que o codificador seja compatível [**com GetValue,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange.**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)

Se [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) não for chamado para \_ CODECAPI AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) para CODECAPI \_ AVEncSliceControlMode poderá retornar **VFW \_ E \_ CODECAPI \_ NO CURRENT \_ \_ VALUE**. [**GetDefaultValue pode**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) retornar **VFW \_ E \_ CODECAPI \_ NO \_ DEFAULT** para CODECAPI \_ AVEncSliceControlMode.

O valor padrão recomendado é 2 (tamanho em linha MB por fatia).

Essa é uma API estática, o que significa que o aplicativo não alterará isso enquanto o codificador estiver em execução.

## <a name="examples"></a>Exemplos


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



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

 

