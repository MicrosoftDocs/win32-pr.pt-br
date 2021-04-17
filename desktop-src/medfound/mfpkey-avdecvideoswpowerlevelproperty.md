---
description: Especifica o nível de energia para o decodificador.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: Propriedade MFPKEY_AVDecVideoSWPowerLevel (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763262"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a>\_Propriedade MFPKEY AVDecVideoSWPowerLevel

Especifica o nível de energia para o decodificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**\_UI4 VT**

## <a name="default-value"></a>Valor padrão

**100**

## <a name="remarks"></a>Comentários

Essa propriedade deve ser definida como um dos valores a seguir.



| Valor | Significado                                                             |
|-------|---------------------------------------------------------------------|
| 0     | O decodificador usa um nível de energia que é otimizado para a vida útil da bateria.  |
| 50    | O decodificador usa um nível de energia equilibrado.                            |
| 100   | O decodificador usa um nível de energia otimizado para qualidade de vídeo. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
