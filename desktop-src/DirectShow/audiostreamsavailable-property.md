---
description: A propriedade AudioStreamsAvailable recupera o número de fluxos de áudio disponíveis no título atual.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propriedade AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825712"
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

Esta propriedade é somente leitura sem valor padrão. O uso principal de vários fluxos de áudio é fornecer as trilhas sonoras do filme em mais de um idioma. Normalmente, nem todos os títulos em um disco têm todos os fluxos de áudio habilitados. Por exemplo, o filme de recursos pode ter trilhas sonoras em três idiomas diferentes, mas os trailers podem ter apenas uma trilha sonora em inglês. Antes que um usuário possa selecionar um fluxo, o aplicativo deve determinar quais fluxos estão disponíveis no título atual. Observe que os fluxos específicos são identificados por um índice de zero a 7.

Os discos geralmente apresentam um menu mostrando as trilhas sonoras disponíveis, permitindo que o usuário selecione o fluxo de áudio a ser habilitado.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



