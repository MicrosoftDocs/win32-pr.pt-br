---
description: Ajusta o brilho.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: Propriedade MFPKEY_COLOR_BRIGHTNESS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a43969dff8d743e493916303c31e3d57760a2b025bfadaeaf8cc03e7e25430d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954646"
---
# <a name="mfpkey_color_brightness-property"></a>Propriedade de brilho de \_ cor do MFPKEY \_

Ajusta o brilho.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="applies-to"></a>Aplica-se A

-   [DSP de transformação de controle de cores](colorcontroltransform.md)

## <a name="remarks"></a>Comentários

O ajuste de brilho é executado pela adição de um valor ao canal Luma.

Essa propriedade tem um intervalo de-127 a 127. Zero indica nenhuma alteração no brilho.

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

 

 
