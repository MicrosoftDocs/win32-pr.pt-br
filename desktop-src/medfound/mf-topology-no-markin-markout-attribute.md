---
description: Especifica se o pipeline apara amostras.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: Atributo MF_TOPOLOGY_NO_MARKIN_MARKOUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165015"
---
# <a name="mf_topology_no_markin_markout-attribute"></a>\_Topologia MF \_ sem \_ marca de marcação \_ atributo de marcação

Especifica se o pipeline apara amostras.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Por padrão, o pipeline corta exemplos para corresponder aos tempos de apresentação corretos. A remoção é feita nos nós de topologia que têm [**a \_ marca de TOPONODE MF \_ \_ aqui**](mf-toponode-markin-here-attribute.md) e os atributos [**MF \_ TOPONODE \_ markout \_ aqui**](mf-toponode-markout-here-attribute.md) . Se a **\_ topologia MF \_ sem \_ marca \_** de marcação atributo de marcação estiver definida como **true** na topologia, o pipeline não cortará amostras e os atributos **MF \_ TOPONODE \_ marking \_ aqui** e **MF \_ TOPONODE \_ markout \_** serão ignorados. Se o atributo não estiver definido ou tiver o valor **false**, o pipeline cortará os exemplos.

Um aplicativo pode definir a **\_ topologia MF \_ sem \_ marca \_** de marcação atributo de marcação como **true** se o aplicativo receber amostras compactadas do pipeline e precisar obter todos os quadros-chave que, de outra forma, podem ser cortados.

O valor padrão desse atributo é **false**.

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

[**\_Mark TOPONODE do MF \_ \_ aqui**](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[**\_marcação de TOPONODE MF \_ \_ aqui**](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




