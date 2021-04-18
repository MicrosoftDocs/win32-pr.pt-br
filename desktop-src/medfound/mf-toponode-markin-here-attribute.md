---
description: Especifica se o pipeline aplica o marca-in neste nó.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: Atributo MF_TOPONODE_MARKIN_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765331"
---
# <a name="mf_toponode_markin_here-attribute"></a>\_TOPONODE MF \_ \_ aqui atributo

Especifica se o pipeline aplica o marca-in neste nó. Mark-in é o ponto em que uma apresentação é iniciada. Se os componentes de pipeline geram dados antes do ponto de marcação, os dados não são renderizados.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

> [!Note]  
> A maioria dos aplicativos não precisa usar esse atributo. A [sessão de mídia](media-session.md) define automaticamente esse atributo, se necessário.

 

Esse atributo se aplica a todos os tipos de nó. Se o atributo for **true**, o pipeline de Media Foundation apara as amostras de saída deste nó para corresponder à hora de início da apresentação. O carregador de topologia define esse atributo ao resolver uma topologia.

É recomendável que exatamente um nó em cada ramificação da topologia tenha esse atributo definido como **true**. Uma ramificação de topologia é definida como o caminho de um nó de origem para um nó de saída. Dentro de um Branch, os atributos [MF \_ TOPONODE \_ markout \_ ](mf-toponode-markout-here-attribute.md) e MF \_ TOPONODE \_ \_ aqui devem ser definidos no mesmo nó do Branch. Eles não podem ser definidos em nós diferentes dentro da mesma ramificação.

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

[**\_marcação de TOPONODE MF \_ \_ aqui**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




