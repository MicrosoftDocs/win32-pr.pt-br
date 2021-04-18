---
title: Network. sourceProtocol
description: A propriedade sourceProtocol recupera o protocolo de origem usado para receber dados.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Network. sourceProtocol Windows Media Player
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763469"
---
# <a name="networksourceprotocol"></a>Network. sourceProtocol

A propriedade **sourceProtocol** recupera o protocolo de origem usado para receber dados.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **sourceProtocol**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

Essa propriedade é definida como "" (cadeia de caracteres vazia) ao reproduzir mídia de um CD ou DVD.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **sourceProtocol** para exibir o protocolo de origem usado para receber dados. As informações são exibidas em um DIV HTML criado com ID = "SP". O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> </dl>

 

 





