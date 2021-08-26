---
description: Ajusta o matiz.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: Propriedade MFPKEY_COLOR_HUE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646d9e3ae0e72e11ae8952d28df9e4e3afc4147eaa7983bd1f0e9c82266ca5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954436"
---
# <a name="mfpkey_color_hue-property"></a>\_Propriedade matiz de cor do MFPKEY \_

Ajusta o matiz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="applies-to"></a>Aplica-se A

-   [DSP de transformação de controle de cores](colorcontroltransform.md)

## <a name="remarks"></a>Comentários

O ajuste de matiz é realizado pela combinação dos valores CB e CR. (Se CB e CR forem plotados em um espaço bidimensional, o ajuste de matiz será realizado girando em volta da origem.)

Essa propriedade tem um intervalo de-127 a 127. Zero indica nenhuma alteração no matiz.

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

 

 
