---
title: Network. maxBandwidth
description: A propriedade maxBandwidth especifica ou recupera a largura de banda máxima permitida.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Network. maxBandwidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752187"
---
# <a name="networkmaxbandwidth"></a>Network. maxBandwidth

A propriedade **maxBandwidth** especifica ou recupera a largura de banda máxima permitida.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **maxBandwidth**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** de leitura/gravação (**longo**).

## <a name="remarks"></a>Comentários

Esta propriedade não tem valor padrão. Seu valor pode ser especificado enquanto o Windows Media Player está em execução, mas a alteração não entrará em vigor até que o item de mídia atual seja liberado abrindo outro ou chamando o *Player*. **fechar**. O Windows Media Player tenta atingir a maior largura de banda possível. Somente no caso do valor que está sendo definido, qualquer redução de largura de banda ocorrerá.

Essa configuração é útil para reduzir a quantidade de largura de banda usada, principalmente no caso de um fluxo de taxa de bits múltipla (MBR). Um fluxo MBR contém vários fluxos com taxas de bits diferentes. Em alguns casos, pode ser desejável usar um fluxo com uma taxa de bits inferior à necessária pelo cliente. Nesse caso, a definição da propriedade **maxBandwidth** selecionará um fluxo de taxa de bits inferior.

Por exemplo, um fluxo MBR pode incluir fluxos codificados a 20 kilobits por segundo (Kbps), 37 kbps e 200 Kbps. Definir a propriedade **maxBandwidth** como 50.000 (50 kbps) selecionará o fluxo de 37 Kbps em vez do fluxo de 200 Kbps.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Player. fechar**](player-close.md)
</dt> </dl>

 

 





