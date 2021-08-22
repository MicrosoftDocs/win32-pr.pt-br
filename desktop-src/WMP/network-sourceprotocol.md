---
title: Network.sourceProtocol
description: A propriedade sourceProtocol recupera o protocolo de origem usado para receber dados.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Network.sourceProtocol Windows Media Player
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
ms.openlocfilehash: f23cba2fdd56c1076110c495f7dab2451b7fa103e1dd0e0253e4f74f4f8ab59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118836201"
---
# <a name="networksourceprotocol"></a>Network.sourceProtocol

A **propriedade sourceProtocol** recupera o protocolo de origem usado para receber dados.

## <a name="syntax"></a>Syntax

*player*. *network*. **sourceProtocol**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres somente **leitura.**

## <a name="remarks"></a>Comentários

Essa propriedade é definida como "" (cadeia de caracteres vazia) ao tocar mídia de um CD ou DVD.

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Rede*. **sourceProtocol para** exibir o protocolo de origem usado para receber dados. As informações são exibidas em um HTML DIV criado com ID = "SP". O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> </dl>

 

 





