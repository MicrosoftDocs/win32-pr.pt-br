---
description: Especifica se o pipeline pode descartar amostras de um nó de topologia.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: Atributo MF_TOPONODE_DISCARDABLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765170"
---
# <a name="mf_toponode_discardable-attribute"></a>\_Atributo de TOPONODE MF \_

Especifica se o pipeline pode descartar amostras de um nó de topologia.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a todos os tipos de nó. Normalmente, você definiria esse atributo em nós de baixo e para indicar que as saídas secundárias não são essenciais.

O valor do atributo é uma matriz de índices para fluxos de saída no nó.

Se esse atributo for definido, o pipeline poderá descartar amostras dos fluxos de saída especificados, se o fluxo estiver atrasado.

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

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> </dl>

 

 




