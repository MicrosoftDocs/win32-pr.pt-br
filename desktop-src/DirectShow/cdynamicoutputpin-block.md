---
description: 'O método Block bloqueia ou desbloqueia o fluxo de dados do PIN. Esse método implementa o método IPinFlowControl:: Block.'
ms.assetid: 8281cd8c-7543-42b5-9a4a-11bdfcb659e3
title: Método CDynamicOutputPin. Block (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Block
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cc0a601ee1adbff9254baeff029c26d0cea359c7b2770b4d518bad916aca09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074280"
---
# <a name="cdynamicoutputpinblock-method"></a>Método CDynamicOutputPin. Block

O `Block` método bloqueia ou desbloqueia o fluxo de dados do PIN. Esse método implementa o método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Block(
   DWORD  dwBlockFlags,
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwBlockFlags* 
</dt> <dd>

Sinalizador que indica se deve bloquear ou desbloquear o PIN. Deve ser um dos seguintes valores: 

Zero: desbloquear o fluxo de dados do PIN.

\_Bloco de \_ controle de fluxo am-PIN \_ \_ : bloqueia o fluxo de dados do PIN.

</dd> <dt>

*hEvent* 
</dt> <dd>

Identificador para um objeto de evento ou **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                                                                    | Descrição                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>                                        | O PIN já está desbloqueado.<br/>                     |
| <dl> <dt>**S \_ OK**</dt> </dl>                                           | Êxito.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                   | Argumento inválido.<br/>                             |
| <dl> <dt>**VFW \_ E \_ PIN \_ já \_ bloqueados**</dt> </dl>                   | O PIN já está bloqueado em outro thread.<br/>     |
| <dl> <dt>**VFW \_ E \_ PIN \_ já \_ bloqueados neste \_ \_ \_ thread**</dt> </dl> | O PIN já está bloqueado no thread de chamada.<br/> |



 

## <a name="remarks"></a>Comentários

Para obter mais informações sobre esse método, consulte [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block). Internamente, esse método chama um dos seguintes métodos protegidos:

-   Bloquear (assíncrono): [ **CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)
-   Bloco (síncrono): [ **CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)
-   Desbloquear: [ **CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)

O desbloqueio é sempre executado de forma síncrona.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




