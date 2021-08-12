---
description: O método get \_ Owner recupera o proprietário da janela atual.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: CBaseControlWindow.get_Owner método (Ctlutil.h)
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
ms.openlocfilehash: 3a64325fddebc410c5a75a5c2fb8811241012feb6a046b9059897f9b13e0206f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660509"
---
# <a name="cbasecontrolwindowget_owner-method"></a>Método CBaseControlWindow.get \_ Owner

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

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="remarks"></a>Comentários

A janela de vídeo pode ser reproduzida em um ambiente de documento. Para fazer isso, a janela deve ser um filho de outra janela (para que ela seja recortada e movida adequadamente). Essa propriedade permite que o proprietário da janela seja definido e recuperado. Quando a janela pertence a outra janela, ela simplesmente chama a função **SetParent** do Microsoft Win32. Um aplicativo que chama essa função alterará os estilos de janela para definir o \_ bit FILHO do WS.

Quando a janela pertence a outra janela, ela encaminha automaticamente determinados conjuntos de mensagens (em particular, mensagens de mouse e teclado). Isso permite que um aplicativo faça uma edição de ponto de contato simples e outras interações.

Essa função membro deve ser chamada por objetos externos por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e, portanto, bloqueia a seção crítica para sincronizar com o filtro associado. Chame a [**função membro CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) para recuperar essa propriedade se não estiver chamando de um objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




