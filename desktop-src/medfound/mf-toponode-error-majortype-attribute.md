---
description: Contém o tipo de mídia principal para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: MF_TOPONODE_ERROR_MAJORTYPE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e32752f74708272c367e3f15b208ed66fb0d476baab75b8032ed028e1b9e4162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875140"
---
# <a name="mf_toponode_error_majortype-attribute"></a>Atributo MF \_ TOPONODE \_ ERROR \_ MAJORTYPE

Contém o tipo de mídia principal para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a todos os tipos de nó.

O carregador de topologia pode definir o atributo . Os aplicativos normalmente leem esse atributo, mas não o configuram.

Para ver uma lista de valores possíveis, consulte [Tipos de mídia principais.](media-type-guids.md)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




