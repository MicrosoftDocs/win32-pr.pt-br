---
title: External. AccountType
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. A Propriedade AccountType recupera o tipo de conta do usuário atual.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- External. AccountType Windows Media Player
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759708"
---
# <a name="externalaccounttype"></a>External. AccountType

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

A propriedade **AccountType** recupera o tipo de conta do usuário atual.

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** somente leitura que representa o tipo de conta. Cadeias de caracteres que representam vários tipos de conta são definidas pelo repositório online.

## <a name="remarks"></a>Comentários

Essa propriedade recupera o tipo de conta chamando o método [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , que é implementado pelo plug-in da loja online. Se o usuário atual estiver conectado à loja online ou o plug-in tiver armazenado em cache as credenciais do usuário, o método **getContentPartnerInfo** poderá determinar o tipo de conta do usuário e retorná-lo ao Windows Media Player. O tipo de conta é uma cadeia de caracteres que o Windows Media Player não interpreta. Em vez disso, o Windows Media Player passa a cadeia de caracteres do plug-in da loja online para o script na página de descoberta da loja online.

Se o usuário atual não estiver conectado à loja online e o plug-in da loja online não tiver credenciais armazenadas em cache para o usuário, essa propriedade recuperará qualquer cadeia de caracteres que o método **getContentPartnerInfo** retornar nessa situação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. userlogado**](external-userloggedin.md)
</dt> </dl>

 

 





