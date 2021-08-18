---
title: Duração da mídia
description: A Propriedade Duration recupera a duração do item de mídia atual em segundos.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Windows Media Player de mídia. duração
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89eab1ffbb8c9f3d48c3f61eb6d831af66b4931ed1d858658eed3fc21d08183
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118796"
---
# <a name="mediaduration"></a>Duração da mídia

A propriedade **Duration** recupera a duração do item de mídia atual em segundos.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **duração**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura ( **duplo**).

## <a name="remarks"></a>Comentários

Se essa propriedade for usada com um item de mídia diferente daquele especificado no *Player*. **currentMedia**, ele não pode conter um valor válido.

para recuperar a duração de arquivos que não estão na biblioteca do usuário, você deve aguardar a Windows Media Player abrir o arquivo; ou seja, o OpenState atual deve ser igual a MediaOpen. Você pode verificar isso manipulando o *Player*. Evento **OpenStateChange** ou verificando periodicamente o valor do *Player*. **OpenState**.

Para listas de reprodução, a duração de cada item de mídia pode ser recuperada quando o item de mídia individual é aberto, em vez de quando a playlist é aberta.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

o exemplo a seguir JScript usa *mídia*. **duração** para exibir o tempo restante no item de mídia atual. Um elemento HTML DIV chamado RemTime exibe as informações. Um temporizador HTML atualiza o texto no elemento DIV a cada segundo.

o código de JScript a seguir inicia o temporizador:


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



o código de JScript a seguir interrompe o temporizador:


```JScript
window.clearInterval(idTmr);
```



Use o *Player*. Evento **PlayStateChange** com uma instrução **switch** para determinar quando iniciar e parar o temporizador.

o código de JScript a seguir é executado cada vez que o temporizador chama a função update:


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Evento Player. PlayStateChange**](player-player-playstatechange.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





