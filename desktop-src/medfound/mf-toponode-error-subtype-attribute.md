---
description: Contém o subtipo de mídia para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: Atributo MF_TOPONODE_ERROR_SUBTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798203"
---
# <a name="mf_toponode_error_subtype-attribute"></a>\_Atributo de \_ subtipo de erro MF TOPONODE \_

Contém o subtipo de mídia para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a todos os tipos de nó.

O carregador de topologia pode definir o atributo. Normalmente, os aplicativos lêem esse atributo, mas não os definem.

Para obter uma lista de valores possíveis, consulte [GUIDs de tipo de mídia](media-type-guids.md).

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

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




