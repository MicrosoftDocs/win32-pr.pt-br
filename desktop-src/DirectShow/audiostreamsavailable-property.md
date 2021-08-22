---
description: A propriedade AudioStreamsAvailable recupera o número de fluxos de áudio disponíveis no título atual.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propriedade AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07025a3a3bf54ad98d32c54ee3c147bc36489822ef451965e1e0e0da8fe586c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586726"
---
# <a name="audiostreamsavailable-property"></a>Propriedade AudioStreamsAvailable

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `AudioStreamsAvailable` propriedade recupera o número de fluxos de áudio disponíveis no título atual.

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro de 1 a 8 que representa o número de fluxos de áudio disponíveis no título atual.

## <a name="remarks"></a>Comentários

Essa propriedade é somente leitura sem valor padrão. O principal uso de vários fluxos de áudio é fornecer filmes de filmes em mais de um idioma. Normalmente, nem todos os títulos em um disco têm todos os fluxos de áudio habilitados. Por exemplo, o filme de recurso pode ter músicas em três idiomas diferentes, mas os trailers podem ter apenas um idioma inglês. Antes que um usuário possa selecionar um fluxo, o aplicativo deve determinar quais fluxos estão disponíveis no título atual. Observe que fluxos específicos são identificados por um índice de zero a 7.

Os discos geralmente apresentam um menu mostrando as trilhas disponíveis, permitindo que o usuário selecione o fluxo de áudio a ser habilitado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



