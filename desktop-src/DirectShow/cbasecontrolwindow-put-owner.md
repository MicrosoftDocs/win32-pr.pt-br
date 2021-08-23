---
description: O método put Owner define a janela pai da janela de vídeo; a janela pai encaminha \_ determinadas mensagens para a janela de vídeo.
ms.assetid: 8ed85cb0-47be-40c1-947a-dd9f7850d867
title: CBaseControlWindow.put_Owner método (Ctlutil.h)
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
ms.openlocfilehash: 8f33e0c26506faea93afc11f51aaba13007c443fc011839efafce436fe9f2b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635886"
---
# <a name="cbasecontrolwindowput_owner-method"></a>Método de Proprietário CBaseControlWindow.put \_

O método define a janela pai da janela `put_Owner` de vídeo; a janela pai encaminha determinadas mensagens para a janela de vídeo.

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

Lidar com a janela pai.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna NOERROR.

## <a name="remarks"></a>Comentários

Internamente, esse método chama a função Microsoft Win32 **SetParent** para definir o novo proprietário e define o estilo da janela pai como WS \_ CHILD. Em seguida, a janela pai encaminhará determinados conjuntos de mensagens (em particular, mensagens de mouse e teclado) para a janela de vídeo.

Depois de definir o proprietário da janela de vídeo, você deve definir o proprietário como **NULL** e o estilo de janela do proprietário como WS \_ OVERLAPPED e WS CLIPCHILDREN antes de liberar o grafo \_ de filtro. Quando você definir o proprietário como **NULL,** esse método desligará o bit filho WS \_ da janela pai. Se você não definir o proprietário como **NULL,** a janela pai continuará passando mensagens para a janela de vídeo e provavelmente ocorrerão erros quando o aplicativo for fechado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




