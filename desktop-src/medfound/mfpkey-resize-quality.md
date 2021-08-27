---
description: Especifica se um algoritmo deve ser usado para produzir um vídeo de qualidade mais alta ou um algoritmo mais rápido.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: MFPKEY_RESIZE_QUALITY propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8aeb59935c8fc3462b713967ed2b14a0adfcf731fa1a71fec434b0e07d4309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973405"
---
# <a name="mfpkey_resize_quality-property"></a>Propriedade MFPKEY \_ RESIZE \_ QUALITY

Especifica se um algoritmo deve ser usado para produzir um vídeo de qualidade mais alta ou um algoritmo mais rápido.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

BOOL da VT \_

## <a name="applies-to"></a>Aplica-se A

-   [DSP do Resizer de Vídeo](videoresizer.md)

## <a name="remarks"></a>Comentários

Use um dos seguintes valores:



| Valor     | Descrição          |
|-----------|----------------------|
| VT \_ FALSE | Algoritmo mais rápido     |
| VT \_ TRUE  | Vídeo de alta qualidade |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
