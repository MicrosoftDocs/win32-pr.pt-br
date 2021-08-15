---
title: Transmissão
description: O atributo Broadcast é um atributo em nível de arquivo que indica se o conteúdo pode ser transmitido. Supõe-se que qualquer conteúdo para o qual nenhum autor de direitos tenha sido atribuído pode ser de difusão legal.
ms.assetid: da2adf16-a9b5-4678-896e-2be8f5ca27e4
keywords:
- Transmitir formato de mídia do Windows
topic_type:
- apiref
api_name:
- Broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b233a74deb71efe041ab5ad2f5e4ffa421d048a70c5b97e8f7ac38499bd18df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086156"
---
# <a name="broadcast"></a>Transmissão

O atributo **Broadcast** é um atributo em nível de arquivo que indica se o conteúdo pode ser transmitido. Supõe-se que qualquer conteúdo para o qual nenhum autor de direitos tenha sido atribuído pode ser de difusão legal.

## <a name="global-constant"></a>Constante global

g \_ wszWMBroadcast

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

Este atributo não pode ser duplicado no nível do arquivo. se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do formato de mídia Windows.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




