---
title: Método external. attemptLogin
description: O método attemptLogin exibe uma caixa de diálogo para que o usuário possa tentar fazer logon na loja online.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- método attemptLogin Windows Media Player
- método attemptLogin Windows Media Player, classe externa
- Classe externa Windows Media Player, método attemptLogin
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794473"
---
# <a name="externalattemptlogin-method"></a>Método external. attemptLogin

O método **attemptLogin** exibe uma caixa de diálogo para que o usuário possa tentar fazer logon na loja online.

## <a name="syntax"></a>Sintaxe


```JScript
External.attemptLogin()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a tentativa de logon resultar em uma alteração de status de logon, o Windows Media Player gerará o evento [OnLoginChange](external-onloginchange-event.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Evento external. OnLoginChange**](external-onloginchange-event.md)
</dt> <dt>

[**External. userlogado**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner:: logon**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**Gerenciando o logon**](managing-login.md)
</dt> </dl>

 

 





