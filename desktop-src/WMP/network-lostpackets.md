---
title: Network. lostPackets
description: A propriedade lostPackets recupera o número de pacotes perdidos.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Network. lostPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751781"
---
# <a name="networklostpackets"></a>Network. lostPackets

A propriedade **lostPackets** recupera o número de pacotes perdidos.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **lostPackets**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="remarks"></a>Comentários

Essa propriedade só é válida para streaming de mídia e será igual a zero ao usar o protocolo HTTP, que é sem perdas.

Os pacotes podem ser perdidos por vários motivos, como o tipo e a qualidade da conexão de rede.

Toda vez que a reprodução é interrompida e reiniciada, essa propriedade é definida como zero. Ele não será redefinido se a reprodução for pausada e reiniciada. Essa propriedade retorna informações válidas somente durante o tempo de execução e somente se o *jogador*. A propriedade de **URL** está definida.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **lostPackets** para exibir o número total de pacotes perdidos durante a reprodução quando o usuário clica em um botão. As informações são exibidas em uma DIV HTML criada com ID = "LP". O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





