---
description: O \_ método Put Owner define a janela pai da janela de vídeo; a janela pai, em seguida, encaminha certas mensagens para a janela de vídeo.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: Método de CBaseControlWindow.put_Owner (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16817d1c3f0fbdf756f6c054b875b8507fd1172a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753753"
---
# <a name="cbasecontrolwindowput_owner-method"></a>Método de proprietário CBaseControlWindow. put \_

O `put_Owner` método define a janela pai da janela de vídeo; a janela pai, em seguida, encaminha certas mensagens para a janela de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Owner(
   OAHWND Owner
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Proprietário* 
</dt> <dd>

Identificador para a janela pai.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna NOERROR.

## <a name="remarks"></a>Comentários

Internamente, esse método chama a função **Setpai** do Microsoft Win32 para definir o novo proprietário e define o estilo da janela pai como WS \_ Child. A janela pai encaminhará certos conjuntos de mensagens (em particular, mensagens do mouse e do teclado) para a janela de vídeo.

Depois de definir o proprietário da janela de vídeo, você deve definir o proprietário como **nulo** e o estilo de janela do proprietário como WS \_ Overlapped e WS \_ CLIPCHILDREN antes de liberar o grafo de filtro. Quando você define o proprietário como **NULL**, esse método desativa o bit do WS-Child da janela pai \_ . Se você não definir o proprietário como **nulo**, a janela pai continuará a passar mensagens para a janela de vídeo e os erros provavelmente ocorrerão quando o aplicativo for fechado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




