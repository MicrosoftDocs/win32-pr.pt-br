---
description: Contém um ponteiro para o descritor de apresentação do caminho de mídia protegido (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Atributo MF_PD_APP_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171029"
---
# <a name="mf_pd_app_context-attribute"></a>\_Atributo de \_ contexto de aplicativo MF PD \_

Contém um ponteiro para o descritor de apresentação do caminho de mídia protegido (PMP).

## <a name="data-type"></a>Tipo de dados

**IUnknown \** _

## <a name="remarks"></a>Comentários

O proxy de origem de mídia, que é criado no processo do PMP, usa esse atributo para armazenar o descritor de apresentação remoto no descritor de apresentação do aplicativo.

O valor desse atributo é um ponteiro para a interface [_ *IMFPresentationDescriptor* *](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

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

[**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




