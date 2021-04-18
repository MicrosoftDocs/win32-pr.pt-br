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
ms.openlocfilehash: bbf9e7d94682f8dbf08850f87954a934fd909afe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105810896"
---
# <a name="broadcast"></a>Transmissão

O atributo **Broadcast** é um atributo em nível de arquivo que indica se o conteúdo pode ser transmitido. Supõe-se que qualquer conteúdo para o qual nenhum autor de direitos tenha sido atribuído pode ser de difusão legal.

## <a name="global-constant"></a>Constante global

g \_ wszWMBroadcast

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ bool**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

Este atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




