---
description: Contém um ponteiro para o descritor de apresentação para a origem da mídia.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: Atributo MF_TOPONODE_PRESENTATION_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bfa43a57bcead1312ba8138ab085771d29a008fe2558ea7c6bfb29121d631bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113700"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a>\_Atributo de \_ descritor de apresentação TOPONODE MF \_

Contém um ponteiro para o descritor de apresentação para a origem da mídia.

## <a name="data-type"></a>Tipo de dados

**IUnknown\***

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de origem (**\_ nó de \_ SOURCESTREAM \_ de topologia MF**).

O valor do atributo é um ponteiro para a interface [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) do descritor de apresentação. Esse atributo é necessário.

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

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




