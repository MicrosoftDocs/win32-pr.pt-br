---
description: A propriedade CurrentAudioStream define ou recupera o número do fluxo de áudio habilitado.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propriedade CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105749820"
---
# <a name="currentaudiostream-property"></a>Propriedade CurrentAudioStream

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CurrentAudioStream` propriedade define ou recupera o número do fluxo de áudio habilitado.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro de 0 a 7 indicando o fluxo de áudio atual.

## <a name="remarks"></a>Comentários

Esta propriedade é de leitura/gravação sem valor padrão. Antes de tentar definir um novo fluxo de áudio, chame [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) para verificar se o fluxo está disponível.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



