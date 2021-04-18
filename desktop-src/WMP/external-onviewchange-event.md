---
title: Evento external. OnViewChange
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O evento OnViewChange ocorre quando a exibição é alterada no Windows Media Player.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Evento external. OnViewChange do Windows Media Player
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796417"
---
# <a name="externalonviewchange-event"></a>Evento external. OnViewChange

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O evento **OnViewChange** ocorre quando a exibição é alterada no Windows Media Player.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Valores possíveis

Essa é uma propriedade somente gravação que especifica o nome da função no script que o Windows Media Player chama quando o evento ocorre.

## <a name="parameters"></a>Parâmetros

A função que manipula esse evento não usa parâmetros.

## <a name="remarks"></a>Comentários

O modo de exibição no Windows Media Player pode ser alterado por qualquer um dos seguintes motivos:

-   O usuário interage com a interface do usuário do Windows Media Player.
-   O usuário interage com uma página de descoberta e o script na página de descoberta chama [external. changeView](external-changeview.md).
-   O usuário interage com uma página de descoberta e o script na página de descoberta chama [external. changeViewOnlineList](external-changeviewonlinelist.md).

Quando a exibição é alterada no Windows Media Player, o Player chama [IWMPContentPartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) para obter a URL da próxima página de descoberta a ser exibida. No entanto, antes de o Player exibir a página nova descoberta, ele gera o evento **OnViewChange** . Se o manipulador de eventos **OnViewChange** chamar [external. cancelNavigate](external-cancelnavigate.md), o Windows Media Player não exibirá a página nova descoberta. Em vez disso, ele continua a exibir a página de descoberta atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeView**](external-changeview.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





