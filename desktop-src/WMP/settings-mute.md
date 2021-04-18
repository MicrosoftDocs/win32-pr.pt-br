---
title: Configurações. mudo
description: A propriedade MUTE especifica e recupera um valor que indica se o áudio está mudo.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Configurações. ativar mudo do Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786152"
---
# <a name="settingsmute"></a>Configurações. mudo

A propriedade **MUTE** especifica e recupera um valor que indica se o áudio está mudo.

## <a name="syntax"></a>Syntax

Player. Settings. mudo

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** de leitura/gravação.



| Valor | Descrição                  |
|-------|------------------------------|
| true  | O áudio está mudo.              |
| false | Padrão. O áudio não está mudo. |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir cria um elemento de caixa de seleção HTML que permite que o usuário ative mudo e mudo de áudio. O objeto de **jogador** foi criado com ID = "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> </dl>

 

 





