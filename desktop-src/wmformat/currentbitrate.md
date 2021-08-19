---
title: CurrentBitrate
description: O atributo CurrentBitrate contém a taxa de bits total atual dos fluxos ativos no arquivo.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Formato de mídia do Windows CurrentBitrate
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 028207ee152acac289da6608c682f5fc14a4fde69603a2aae05b841d0cfb46ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027944"
---
# <a name="currentbitrate"></a>CurrentBitrate

O atributo CurrentBitrate contém a taxa de bits total atual dos fluxos ativos no arquivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>Tipo de Dados

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Comentários

Esse é um atributo codificado.

O valor recuperado para **CurrentBitrate** é diferente dependendo do objeto usado. No objeto leitor ou de leitor síncrono, o valor é a taxa de bits real no momento da chamada. No objeto do editor de metadados, o valor é a taxa média de bits do arquivo.

A taxa de bits real de um arquivo é igual às taxas de bits de todos os fluxos ativos mais alguma sobrecarga. Esse é o valor que é, por exemplo, exibido ao tocar um arquivo com o Windows Media Player.

Esse atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK Windows Formato de Mídia.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




