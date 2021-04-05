---
description: Contém o código de erro da falha de conexão mais recente para este nó topologia.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: Atributo MF_TOPONODE_ERRORCODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090868"
---
# <a name="mf_toponode_errorcode-attribute"></a>\_Atributo MF TOPONODE \_ ERRORCODE

Contém o código de erro da falha de conexão mais recente para este nó topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Ttreat como um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Esse atributo se aplica a todos os tipos de nó.

O valor desse atributo é um valor **HRESULT** .

A sessão de mídia ou o carregador de topologia pode definir o atributo. Normalmente, os aplicativos lêem esse atributo, mas não os definem.

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

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




