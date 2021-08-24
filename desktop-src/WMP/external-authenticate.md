---
title: Método external. Authenticate
description: O método Authenticate inicia uma tentativa de autenticar o usuário.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- Windows Media Player do método de autenticação
- método de autenticação Windows Media Player, classe externa
- classe externa Windows Media Player, método de autenticação
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b72c4d20cdd8232746175d966856a616bca9629657ca66c35727b8af8e21178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649546"
---
# <a name="externalauthenticate-method"></a>Método external. Authenticate

O método **Authenticate** inicia uma tentativa de autenticar o usuário.

## <a name="syntax"></a>Sintaxe


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AuthenticationIndex* \[ no\]
</dt> <dd>

**Número** (**longo**) que especifica o índice de uma página da Web de autenticação com êxito.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Determinados links em uma página de descoberta têm destinos que devem ser exibidos somente depois que o usuário tiver sido autenticado. a página de descoberta, Windows Media Player e o plug-in da loja online usam as seguintes etapas para autenticar o usuário e exibir a página da web de destino:

1.  O script em uma página de descoberta chama o *externo*. método **Authenticate** .
2.  Windows Media Player exibe uma caixa de diálogo para obter um nome de usuário e senha.
3.  Windows Media Player chama [IWMPContentPartner:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), que inicia a tentativa de autenticação e retorna imediatamente.
4.  Quando a tentativa de autenticação for concluída, o plug-in do repositório online chamará [IWMPContentPartnerCallback:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passando wmpcnAuthResult e um valor booliano que indica se a tentativa foi bem-sucedida.
5.  se a tentativa de autenticação foi bem-sucedida, Windows Media Player chama [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passando g \_ szItemInfo \_ AuthenticationSuccessURL, para obter a URL de uma página da web de autenticação-êxito. nesta chamada, Windows Media Player passa o mesmo índice passado pela página de descoberta para o *externo*. método **Authenticate** .
6.  Windows Media Player exibe a página da web autenticação-êxito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External. userlogado**](external-userloggedin.md)
</dt> </dl>

 

 





