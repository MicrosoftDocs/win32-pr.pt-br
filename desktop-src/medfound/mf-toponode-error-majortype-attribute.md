---
description: Contém o tipo de mídia principal para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: Atributo MF_TOPONODE_ERROR_MAJORTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771403"
---
# <a name="mf_toponode_error_majortype-attribute"></a>MF \_ TOPONODE \_ erro de \_ atributo majortype

Contém o tipo de mídia principal para um nó de topologia. Esse atributo é definido quando a topologia não é carregada porque não foi possível encontrar o decodificador correto.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a todos os tipos de nó.

O carregador de topologia pode definir o atributo. Normalmente, os aplicativos lêem esse atributo, mas não os definem.

Para obter uma lista de valores possíveis, consulte [tipos de mídia principais](media-type-guids.md).

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

 

 




