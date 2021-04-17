---
title: External. userlogado
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | External. userlogado
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- External. userlogado no Windows Media Player
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811101"
---
# <a name="externaluserloggedin"></a>External. userlogado

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **Userlogind** recupera um valor que indica se o usuário está conectado à loja online.

## <a name="syntax"></a>Syntax

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um **booliano** somente leitura. **Verdadeiro** indica que o usuário está conectado e **false** indica que o usuário está desconectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**Evento external. OnLoginChange**](external-onloginchange-event.md)
</dt> </dl>

 

 





