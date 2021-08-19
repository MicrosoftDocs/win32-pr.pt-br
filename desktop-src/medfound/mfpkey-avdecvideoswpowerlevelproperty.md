---
description: Especifica o nível de energia do decodificador.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce376a370ea6488c87c0266319de7e9bde0a94edab7137a81f015f416ea9fc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874060"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>Propriedade MFPKEY \_ AVDecVideoSWPowerLevel

Especifica o nível de energia do decodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**VT \_ UI4**

## <a name="default-value"></a>Valor padrão

**100**

## <a name="remarks"></a>Comentários

Essa propriedade deve ser definida como um dos valores a seguir.



| Valor | Significado                                                             |
|-------|---------------------------------------------------------------------|
| 0     | O decodificador usa um nível de energia otimizado para a vida útil da bateria.  |
| 50    | O decodificador usa um nível de energia balanceado.                            |
| 100   | O decodificador usa um nível de energia otimizado para qualidade de vídeo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
