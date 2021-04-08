---
description: Especifica o modo de controle de fatia. Os valores válidos são 0, 1 e 2.
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: Propriedade CODECAPI_AVEncSliceControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920636"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>\_Propriedade CODECAPI AVEncSliceControlMode

Especifica o modo de controle de fatia. Os valores válidos são 0, 1 e 2.

## <a name="data-type"></a>Tipo de dados

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncSliceControlMode**

## <a name="property-value"></a>Valor da propriedade

Valores do modo de controle de fatia:



| Valor                                                                        | Significado                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Definir esse valor como 0 indica que a propriedade [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de macroblocos por fatia.<br/>     |
| <dl> <dt>1</dt> </dl> | Definir esse valor como 1 indica que a propriedade [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de bits por fatia.<br/>            |
| <dl> <dt>2</dt> </dl> | Definir esse valor como 2 indica que a propriedade [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) especificará o tamanho da fatia em unidades de macrobloco linhas por fatia.<br/> |



 

O codificador retorna os valores que ele suporta.

## <a name="remarks"></a>Comentários

**Codificadores H. 264/AVC:**

É recomendável que o codificador ofereça suporte a [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).

Se [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) não for chamado para CODECAPI \_ AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) para CODECAPI \_ AVEncSliceControlMode poderá retornar **VFW \_ E \_ CODECAPI \_ nenhum \_ \_ valor atual**. [**Getdefaultvalue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) pode retornar **VFW \_ E \_ CODECAPI \_ nenhum \_ padrão** para CODECAPI \_ AVEncSliceControlMode.

O valor padrão recomendado é 2 (tamanho em MB de linha por fatia).

Essa é uma API estática, o que significa que o aplicativo ganhou t altere isso enquanto o codificador estiver em execução.

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
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

