---
title: Network. framesSkipped
description: A propriedade framesSkipped recupera o número total de quadros ignorados durante a reprodução.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Network. framesSkipped Windows Media Player
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810782"
---
# <a name="networkframesskipped"></a>Network. framesSkipped

A propriedade **framesSkipped** recupera o número total de quadros ignorados durante a reprodução.

## <a name="syntax"></a>Syntax

*Player*. *rede*. **framesSkipped**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa a *rede*. **framesSkipped** para exibir o número total de quadros ignorados durante a reprodução quando o usuário clica em um botão. As informações são exibidas em uma DIV HTML criada com ID = "FS". O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

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

 

 





