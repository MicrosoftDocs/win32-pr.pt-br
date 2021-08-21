---
description: O método GetChannelContent recupera um valor que indica o tipo de conteúdo no canal especificado no fluxo especificado.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Método GetChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0353ebda6469627b5f41209b780fc1403c51940705be72d6acaa139d8320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812486"
---
# <a name="getkaraokechannelcontent-method"></a>Método GetChannelContent

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O método recupera um valor que indica o tipo de conteúdo no `GetKaraokeChannelContent` canal especificado no fluxo especificado.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica o fluxo de áudio como um Inteiro.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*Ichannel*
</dt> <dd>

Especifica o canal como um Inteiro. Os valores possíveis para cada canal são:



| Valor  | Descrição    |
|--------|----------------|
| 0x0001 | Guia Vocal 1  |
| 0x0002 | Guia Vocal 2  |
| 0x0004 | Guide Guide 1 |
| 0x0008 | Guide Guide Guide 2 |
| 0x0010 | Guia A |
| 0x0020 | Guide Melody B |
| 0x0040 | Efeito de som A |
| 0x0080 | Efeito de som B |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro cujos bits individuais especificam o conteúdo do canal de ltda.

## <a name="remarks"></a>Comentários

A numeração do canal de áudio de DVD é baseada em zero, portanto, os canais 2, 3 e 4 são os canais auxiliares. Depois que o método retornar, execute uma operação AND bit a bit no *iContent* para determinar o conteúdo de cada canal. Como um único canal pode ter mais de um tipo de conteúdo gravado nele, você deve testar todos os valores possíveis mesmo depois que uma combinação for encontrada.

Depois que o usuário souber o conteúdo de cada canal, ele deverá ser capaz de ajustar o volume ou ativar ou desativar os canais individuais conforme necessário. Implemente essa funcionalidade em seu aplicativo usando a [**propriedade TelegrameAudioPresentationMode.**](karaokeaudiopresentationmode-property.md)

> [!Note]  
> Para reproduzir discos de DirectShow 8, o decodificador de áudio no sistema do usuário deve ser compatível com a implementação DirectShow 8.

 

 

 



