---
description: O método GetFlags recupera os sinalizadores de contexto associados ao comando adiado.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Método CDeferredCommand.GetFlags (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c3ee5826c1b4ff81f90c86a6db4517aafc41313e53672486c41ab4847e82674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910186"
---
# <a name="cdeferredcommandgetflags-method"></a>Método CDeferredCommand.GetFlags

O `GetFlags` método recupera os sinalizadores de contexto associados ao comando adiado.

## <a name="syntax"></a>Sintaxe


```C++
short GetFlags();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna uma destas opções:



| Código de retorno                                                                                             | Descrição                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MÉTODO \_ DISPATCH**</dt> </dl>         | Execute o membro como um método. Se uma propriedade tiver o mesmo nome, este e o sinalizador DISPATCH \_ PROPERTYGET poderão ser definidos.<br/>                                               |
| <dl> <dt>**DISPATCH \_ PROPERTYGET**</dt> </dl>    | O membro está sendo recuperado como uma propriedade ou membro de dados.<br/>                                                                                                         |
| <dl> <dt>**DISPATCH \_ PROPERTYPUT**</dt> </dl>    | O membro está sendo alterado como uma propriedade ou membro de dados.<br/>                                                                                                           |
| <dl> <dt>**DISPATCH \_ PROPERTYPUTREF**</dt> </dl> | O membro está sendo alterado por meio de uma atribuição de referência, em vez de uma atribuição de valor. Esse sinalizador é válido somente quando a propriedade aceita uma referência a um objeto .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




