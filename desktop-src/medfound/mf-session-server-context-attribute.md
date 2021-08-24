---
description: Permite que duas instâncias da sessão de mídia compartilhem o mesmo processo PMP (caminho de mídia protegido).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Atributo MF_SESSION_SERVER_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc9674a2e25a7cdfd0a88ebcc43c18d6fd636bf22116f76a24255b55f857a677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102332"
---
# <a name="mf_session_server_context-attribute"></a>\_Atributo de \_ contexto de servidor de sessão MF \_

Permite que duas instâncias da sessão de mídia compartilhem o mesmo processo PMP (caminho de mídia protegido).

## <a name="data-type"></a>Tipo de dados

**IUnknown\***

## <a name="remarks"></a>Comentários

Use esse atributo se você quiser criar a sessão de mídia do PMP em um processo de PMP existente. O valor do atributo é um ponteiro para a interface [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Atributos de sessão de mídia](media-session-attributes.md)
</dt> </dl>

 

 




