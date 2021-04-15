---
description: O identificador de classe (CLSID) da Media Foundation transformação (MFT) associada a esse nó de topologia.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Atributo MF_TOPONODE_TRANSFORM_OBJECTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502111"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>\_Atributo de \_ OBJECTID de transformação MF TOPONODE \_

O identificador de classe (CLSID) da Media Foundation transformação (MFT) associada a esse nó de topologia.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de transformação (**\_ nó de \_ transformação \_ de topologia MF**).

Os aplicativos podem usar esse atributo para inicializar um nó de Transbase. Se você definir esse atributo, não precisará chamar [**IMFTopologyNode:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) com um ponteiro para um objeto de ativação ou MFT. Por outro lado, se você chamar **setObject**, não precisará definir esse atributo. Para obter mais informações, consulte [criando topologias](creating-topologies.md).

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

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Criando topologias](creating-topologies.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




