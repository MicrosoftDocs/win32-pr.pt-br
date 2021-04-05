---
description: O método GetKaraokeChannelAssignment recupera um valor que indica como os canais do karaokê são atribuídos aos alto-falantes.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Método GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103826060"
---
# <a name="getkaraokechannelassignment-method"></a>Método GetKaraokeChannelAssignment

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetKaraokeChannelAssignment` método recupera um valor que indica como os canais do karaokê são atribuídos aos alto-falantes.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Especifica o fluxo de áudio como um inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro que indica a atribuição de viva-voz para o fluxo especificado.



| Código de retorno | Descrição                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | O fluxo é atribuído aos alto-falantes esquerdo e direito.                  |
| 3           | O fluxo é atribuído aos alto-falantes esquerdo, direito e intermediário.         |
| 4           | O fluxo é atribuído aos alto-falantes esquerdo, direito e Audio1.         |
| 5           | O fluxo é atribuído aos alto-falantes esquerdo, direito, médio e Audio1. |
| 6           | O fluxo é atribuído aos alto-falantes esquerdo, direito e Audio2.         |
| 7           | O fluxo é atribuído aos alto-falantes esquerdo, direito, médio e Audio2. |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



