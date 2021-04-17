---
description: O método GetFlags recupera os sinalizadores de contexto associados ao comando adiado.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Método CDeferredCommand. GetFlags (Ctlutil. h)
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
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770103"
---
# <a name="cdeferredcommandgetflags-method"></a>Método CDeferredCommand. GetFlags

O `GetFlags` método recupera os sinalizadores de contexto associados ao comando adiado.

## <a name="syntax"></a>Sintaxe


```C++
short GetFlags();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna uma destas opções:



| Código de retorno                                                                                             | Descrição                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**método de expedição \_**</dt> </dl>         | Execute o membro como um método. Se uma propriedade tiver o mesmo nome, isso e o \_ sinalizador PROPERTYGET de expedição poderão ser definidos.<br/>                                               |
| <dl> <dt>**PROPERTYGET de expedição \_**</dt> </dl>    | O membro está sendo recuperado como uma propriedade ou um membro de dados.<br/>                                                                                                         |
| <dl> <dt>**PROPERTYPUT de expedição \_**</dt> </dl>    | O membro está sendo alterado como um membro de propriedade ou de dados.<br/>                                                                                                           |
| <dl> <dt>**PROPERTYPUTREF de expedição \_**</dt> </dl> | O membro está sendo alterado por meio de uma atribuição de referência, em vez de uma atribuição de valor. Esse sinalizador é válido somente quando a propriedade aceita uma referência a um objeto.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




