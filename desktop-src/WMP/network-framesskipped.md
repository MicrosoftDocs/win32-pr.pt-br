---
title: Network.framesSkipped
description: A propriedade framesSkipped recupera o número total de quadros ignorados durante a reprodução.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Network.framesSkipped Windows Media Player
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
ms.openlocfilehash: 1031585feae5fa2c7fdd9f5fb64bf958e77b8029d502f3e99476024276a652cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901666"
---
# <a name="networkframesskipped"></a>Network.framesSkipped

A **propriedade framesSkipped** recupera o número total de quadros ignorados durante a reprodução.

## <a name="syntax"></a>Syntax

*player*. *network*. **framesSkipped**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**).

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Rede*. **framesSkipped para** exibir o número total de quadros ignorados durante a reprodução quando o usuário clica em um botão. As informações são exibidas em um HTML DIV criado com ID = "FS". O **objeto** Player foi criado com ID = "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

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

 

 





