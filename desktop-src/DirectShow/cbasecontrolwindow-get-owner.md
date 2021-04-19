---
description: O \_ método Get Owner recupera o proprietário da janela atual.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: Método de CBaseControlWindow.get_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764584"
---
# <a name="cbasecontrolwindowget_owner-method"></a>Método de proprietário CBaseControlWindow. get \_

O `get_Owner` método recupera o proprietário da janela atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Proprietário* 
</dt> <dd>

Ponteiro para o proprietário da janela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

A janela de vídeo pode reproduzir em um ambiente de documento. Para fazer isso, a janela deve se tornar um filho de outra janela (para que seja recortada e movida adequadamente). Essa propriedade permite que o proprietário da janela seja definido e recuperado. Quando a janela pertence a outra janela, ela simplesmente chama a função **setpai** do Microsoft Win32. Um aplicativo que chama essa função alterará os estilos de janela para definir o bit do WS- \_ Child em.

Quando a janela pertence a outra janela, ela encaminha automaticamente determinados conjuntos de mensagens (em particular, mensagens do mouse e do teclado). Isso permite que um aplicativo faça uma edição de ponto de acesso simples e outras interações.

Essa função de membro deve ser chamada por objetos externos por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e, portanto, bloqueia a seção crítica para sincronizar com o filtro associado. Chame a função de membro [**CBaseControlWindow:: GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) para recuperar essa propriedade se não estiver chamando de um objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




