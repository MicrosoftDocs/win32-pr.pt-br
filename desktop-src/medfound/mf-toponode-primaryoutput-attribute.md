---
description: Indica qual saída é a saída primária em um nó de t.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: Atributo MF_TOPONODE_PRIMARYOUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296482"
---
# <a name="mf_toponode_primaryoutput-attribute"></a>\_Atributo MF TOPONODE \_ PrimaryOutput porque

Indica qual saída é a saída primária em um nó de t.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica a nós de "t" (**\_ nó de \_ t \_ da topologia MF**).

O valor desse atributo é o índice de base zero de uma conexão de saída neste nó de alto-t. Esse valor indica qual saída é o fluxo de saída primário. O pipeline aguarda uma solicitação da saída primária antes de processar solicitações de outras saídas.

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

 

 




