---
description: Especifica se um algoritmo que produz vídeo de qualidade superior ou um algoritmo mais rápido é usado.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: Propriedade MFPKEY_RESIZE_QUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771402"
---
# <a name="mfpkey_resize_quality-property"></a>\_Propriedade de qualidade de redimensionamento MFPKEY \_

Especifica se um algoritmo que produz vídeo de qualidade superior ou um algoritmo mais rápido é usado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="applies-to"></a>Aplica-se A

-   [DSP de redimensionador de vídeo](videoresizer.md)

## <a name="remarks"></a>Comentários

Use um dos seguintes valores:



| Valor     | Descrição          |
|-----------|----------------------|
| VT \_ falso | Algoritmo mais rápido     |
| VT \_ verdadeiro  | Vídeo de qualidade superior |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
