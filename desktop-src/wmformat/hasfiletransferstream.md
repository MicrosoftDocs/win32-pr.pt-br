---
title: HasFileTransferStream
description: O atributo HasFileTransferStream é um atributo em nível de arquivo que especifica se o arquivo contém fluxos de transferência de arquivo.
ms.assetid: 5a671fb7-cd79-4ea8-8aed-63402dc008d3
keywords:
- Formato de mídia do Windows HasFileTransferStream
topic_type:
- apiref
api_name:
- HasFileTransferStream
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b239a02968b7dc3a2c8f9c06588e8e6a5545fb3d252c719d65322c4d0e259619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118028668"
---
# <a name="hasfiletransferstream"></a>HasFileTransferStream

O atributo **HasFileTransferStream** é um atributo em nível de arquivo que especifica se o arquivo contém fluxos de transferência de arquivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMHasFileTransferStream

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

Este atributo não pode ser duplicado no nível do arquivo. se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do formato de mídia Windows.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




