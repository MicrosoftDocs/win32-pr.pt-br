---
description: Ajusta a saturação.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: Propriedade MFPKEY_COLOR_SATURATION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b357521327bc913a0ace6b630cb9f2a27b553c3dfc8303e1a6bd9af218c5b743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954396"
---
# <a name="mfpkey_color_saturation-property"></a>Propriedade de saturação de \_ cor MFPKEY \_

Ajusta a saturação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="applies-to"></a>Aplica-se A

-   [DSP de transformação de controle de cores](colorcontroltransform.md)

## <a name="remarks"></a>Comentários

O ajuste de saturação é executado multiplicando os valores CB e CR por uma constante.

Essa propriedade tem um intervalo de-127 a 127. Zero indica nenhuma alteração na saturação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
