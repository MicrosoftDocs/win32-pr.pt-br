---
description: Especifica se a sessão de mídia usa a preversão no coletor de mídia representado por esse nó de topologia.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: Atributo MF_TOPONODE_DISABLE_PREROLL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752157"
---
# <a name="mf_toponode_disable_preroll-attribute"></a>\_TOPONODE de \_ \_ desrollização de DESABILITAção de MF

Especifica se a sessão de mídia usa a preversão no coletor de mídia representado por esse nó de topologia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de saída (**\_ nó de \_ saída \_ da topologia MF**).

Se o valor desse atributo for **true**, a sessão de mídia não preverterá nenhum dado para o coletor de mídia, mesmo que o coletor de mídia exponha a interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) . Se o valor for **false**, a sessão de mídia preverterá os dados se o coletor de mídia implementar **IMFMediaSinkPreroll**. O valor padrão é **false**.

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

 

 




