---
title: Método external. cancelNavigate
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. | Método external. cancelNavigate
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- Windows Media Player do método cancelNavigate
- método cancelNavigate Windows Media Player, classe externa
- classe externa Windows Media Player, método cancelNavigate
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152594a427282a27c493f33f648b8a889a855f40a5fb13de69b7cc342099eed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649426"
---
# <a name="externalcancelnavigate-method"></a>Método external. cancelNavigate

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

o método **cancelNavigate** informa Windows Media Player que ele não deve exibir uma nova página de descoberta, embora a exibição tenha sido alterada no Player.

## <a name="syntax"></a>Sintaxe


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

quando a exibição é alterada no Windows Media Player, o Player chama o plug-in da loja online para determinar qual página de descoberta exibir em seguida. Em alguns casos, no entanto, a loja online pode querer que o Player continue exibindo a página de descoberta existente. O processo a seguir determina se o Player exibe uma nova página de descoberta:

1.  Uma ação do usuário, na interface do usuário do Player ou na página descoberta, solicita que o Player altere sua exibição.
2.  O Player chama o método [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) do plug-in para determinar qual página de descoberta exibir em seguida. O Player armazena a URL da nova página de descoberta, mas não exibe a página nova descoberta neste momento.
3.  O Player gera o evento [OnViewChange](external-onviewchange-event.md) .
4.  Se o manipulador de eventos **OnViewChange** na página de descoberta chamar **CancelNavigate**, o Player não exibirá a página nova descoberta (determinada na etapa 2). Em vez disso, ele continua a exibir a página de descoberta existente. Se o manipulador de eventos **OnViewChange** não chamar **CancelNavigate**, o Player exibirá a página nova descoberta.

Por exemplo, suponha que o Player esteja exibindo atualmente a exibição de um álbum com determinada faixa selecionada. Suponha também que a página de descoberta atual é a página que representa o álbum inteiro. Se o usuário clicar em uma faixa diferente do mesmo álbum, a exibição do jogador será levemente alterada para mostrar que a nova faixa está selecionada. Mas não há necessidade de exibir uma nova página de descoberta. A página de descoberta que representa todo o álbum ainda é a página apropriada para o Player exibir.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





