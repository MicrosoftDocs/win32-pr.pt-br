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
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105808273"
---
# <a name="currentbitrate"></a>CurrentBitrate

O atributo CurrentBitrate contém a taxa de bits total atual dos fluxos ativos no arquivo.

## <a name="global-constant"></a>Constante global

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>Tipo de Dados

**WMT \_ tipo \_ DWORD**

## <a name="remarks"></a>Comentários

Este é um atributo codificado.

O valor recuperado para **CurrentBitrate** é diferente, dependendo do objeto usado. No objeto leitor ou leitor síncrono, o valor é a taxa de bits real no momento da chamada. No objeto editor de metadados, o valor é a taxa média de bits do arquivo.

A taxa de bits real de um arquivo é igual às taxas de bits de todos os fluxos ativos mais alguma sobrecarga. Esse é o valor que é, por exemplo, exibido ao reproduzir um arquivo com o Windows Media Player.

Este atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK do Windows Media Format.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




