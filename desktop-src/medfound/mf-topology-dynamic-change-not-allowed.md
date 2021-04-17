---
description: Especifica se a sessão de mídia tenta modificar a topologia quando o formato de um fluxo é alterado.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Atributo MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461080"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>\_Atributo de \_ alteração dinâmica de topologia MF \_ \_ não \_ permitido

Especifica se a sessão de mídia tenta modificar a topologia quando o formato de um fluxo é alterado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

Esse atributo controla como a sessão de mídia responde se o formato de um fluxo for alterado durante o streaming.

Se o formato for alterado e o \_ \_ atributo alteração dinâmica de topologia MF \_ \_ não \_ permitido for **falso**, a sessão de mídia poderá inserir novos nós na topologia para corresponder ao novo formato. Por exemplo, se o tamanho do vídeo for alterado, a sessão de mídia poderá adicionar uma Media Foundation transformação (MFT) que redimensiona o vídeo. Caso contrário, se o atributo for **true**, a sessão de mídia não modificará a topologia.

O valor padrão desse atributo é **false**. O valor recomendado é **false**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




