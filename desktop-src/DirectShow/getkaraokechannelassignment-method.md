---
description: O método GetTifokeChannelAssignment recupera um valor que indica como os canais de sinal são atribuídos aos alto-falantes.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Método GetChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010e8112ece9b3fc66831055995ebf46657d4216942ac3b9dee05b1b68d18761
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812546"
---
# <a name="getkaraokechannelassignment-method"></a>Método GetChannelAssignment

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `GetKaraokeChannelAssignment` método recupera um valor que indica como os canais de ltda são atribuídos aos alto-falantes.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Especifica o fluxo de áudio como um Inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um inteiro que indica a atribuição do locutor para o fluxo especificado.



| Código de retorno | Descrição                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | O fluxo é atribuído aos alto-falantes esquerdo e direito.                  |
| 3           | O fluxo é atribuído aos alto-falantes esquerdo, direito e intermediário.         |
| 4           | O fluxo é atribuído aos alto-falantes esquerdo, direito e audio1.         |
| 5           | O fluxo é atribuído aos alto-falantes esquerdo, direito, intermediário e audio1. |
| 6           | O fluxo é atribuído aos alto-falantes esquerdo, direito e audio2.         |
| 7           | O fluxo é atribuído aos alto-falantes esquerdo, direito, intermediário e audio2. |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**LtdeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



