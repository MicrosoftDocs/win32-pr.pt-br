---
description: Especifica se o pipeline aplica a marcação neste nó. A marcação é o ponto em que uma apresentação termina. Se os componentes de pipeline geram dados além do ponto de marcação, os dados não são renderizados.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: Atributo MF_TOPONODE_MARKOUT_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798469"
---
# <a name="mf_toponode_markout_here-attribute"></a>\_Atributo de \_ marcação MF TOPONODE \_ aqui

Especifica se o pipeline aplica a marcação neste nó. A marcação é o ponto em que uma apresentação termina. Se os componentes de pipeline geram dados além do ponto de marcação, os dados não são renderizados.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo se aplica a todos os tipos de nó.

Se esse atributo for **true**, o pipeline de Media Foundation apara as amostras de saída deste nó para corresponder à hora de parada da apresentação. O carregador de topologia define esse atributo ao resolver uma topologia. A maioria dos aplicativos não precisa definir ou recuperar esse atributo.

É recomendável que exatamente um nó em cada ramificação da topologia tenha esse atributo definido como **true**. Uma ramificação de topologia é definida como o caminho de um nó de origem para um nó de saída. Dentro de um Branch, os \_ atributos MF TOPONODE \_ markout \_ e [MF \_ TOPONODE \_ \_ aqui](mf-toponode-markin-here-attribute.md) devem ser definidos no mesmo nó do Branch. Eles não podem ser definidos em nós diferentes dentro da mesma ramificação.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**\_Mark TOPONODE do MF \_ \_ aqui**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




