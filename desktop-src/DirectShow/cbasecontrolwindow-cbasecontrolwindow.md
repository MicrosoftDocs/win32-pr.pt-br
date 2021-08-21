---
description: Construtor de CBaseControlWindow. CBaseControlWindow-método de construtor.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Construtor CBaseControlWindow. CBaseControlWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4944d121c4fe99ee36c893a4d51ca0cd72344dfa47dde17629f5ca2a1ce3fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660761"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a>Construtor CBaseControlWindow. CBaseControlWindow

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o objeto de filtro de mídia proprietário.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Ponteiro para a seção crítica a ser usada para bloqueio.

</dd> <dt>

*pName* 
</dt> <dd>

Ponteiro para a descrição do objeto.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** de controle, se o objeto fizer parte de uma agregação; caso contrário, deve ser **NULL**.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor HRESULT que indica o êxito ou a falha do método de construtor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




