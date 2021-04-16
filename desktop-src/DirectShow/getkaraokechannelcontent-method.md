---
description: O método GetKaraokeChannelContent recupera um valor que indica o tipo de conteúdo no canal do karaokê especificado no fluxo especificado.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Método GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105768644"
---
# <a name="getkaraokechannelcontent-method"></a>Método GetKaraokeChannelContent

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetKaraokeChannelContent` método recupera um valor que indica o tipo de conteúdo no canal do karaokê especificado no fluxo especificado.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica o fluxo de áudio como um inteiro.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*
</dt> <dd>

Especifica o canal como um inteiro. Os valores possíveis para cada canal são:



| Valor  | Descrição    |
|--------|----------------|
| 0x0001 | Guia vocal 1  |
| 0x0002 | Guia vocal 2  |
| 0x0004 | Guia de melodia 1 |
| 0x0008 | Guia de melodia 2 |
| 0x0010 | Guia de melodia A |
| 0x0020 | Guia de melodia B |
| 0x0040 | Efeito de som A |
| 0x0080 | Efeito de som B |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro cujos bits individuais especificam o conteúdo do canal do karaokê.

## <a name="remarks"></a>Comentários

A numeração do canal de áudio de DVD é baseada em zero, portanto, os canais 2, 3 e 4 são os canais auxiliares do karaokê. Depois que o método retornar, execute uma operação AND bit a bit em *iContent* para determinar o conteúdo de cada canal. Como um único canal pode ter mais de um tipo de conteúdo registrado nele, você deve testar todos os valores possíveis mesmo depois que uma correspondência for encontrada.

Depois que o usuário conhece o conteúdo de cada canal, ele deve ser capaz de ajustar o volume ou ativar ou desativar os canais individuais, conforme necessário. Implemente essa funcionalidade em seu aplicativo usando a propriedade [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) .

> [!Note]  
> Para reproduzir discos do karaokê, o decodificador de áudio no sistema do usuário deve ser compatível com a implementação do karaokê do DirectShow 8.

 

 

 



