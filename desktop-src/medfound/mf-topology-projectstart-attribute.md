---
description: Especifica a hora de parada de uma topologia, em relação ao início da primeira topologia na sequência.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: Atributo MF_TOPOLOGY_PROJECTSTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827620"
---
# <a name="mf_topology_projectstart-attribute"></a>\_Atributo PROJECTSTART da topologia MF \_

Especifica a hora de parada de uma topologia, em relação ao início da primeira topologia na sequência.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como um valor de **LONGLONG** .

## <a name="remarks"></a>Comentários

O valor é fornecido em unidades de 100 nanossegundos.

Se a sessão de mídia tiver sido criada com o atributo de [**\_ \_ \_ tempo global de sessão MF**](mf-session-global-time-attribute.md) igual a **true**, todas as topologias deverão conter o atributo **\_ \_ PROJECTSTART da topologia MF** . Caso contrário, as topologias não devem conter o atributo **\_ \_ PROJECTSTART da topologia MF** . Para obter mais informações, consulte [tempos de apresentação da sequência](sequence-presentation-times.md).

Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.

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

[Tempos de apresentação da sequência](sequence-presentation-times.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> <dt>

[**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**\_PROJECTSTOP de topologia MF \_**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




