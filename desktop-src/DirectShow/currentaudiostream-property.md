---
description: A propriedade CurrentAudioStream define ou recupera o número do fluxo de áudio habilitado.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propriedade CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd814d5b560ed55ea312fbebb8678c67b1422b0cf3d47917fbf772f56a0d3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075966"
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

Essa propriedade é de leitura/gravação sem valor padrão. Antes de tentar definir um novo fluxo de áudio, chame [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) para verificar se o fluxo está disponível.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



