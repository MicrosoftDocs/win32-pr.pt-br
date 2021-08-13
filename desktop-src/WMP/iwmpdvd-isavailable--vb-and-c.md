---
title: IWMPDVD. IsAvailable (VB e C)
description: A propriedade IsAvailable (o \_ método Get IsAvailable em C \) Obtém um valor que indica se um tipo de informação especificado está disponível ou uma ação especificada pode ser executada.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. IsAvailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78c9dda7bff764752dc55524000ccd3695863afe69dcf45c2ed971c9c0373fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415907"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a>IWMPDVD. IsAvailable (VB e C#)

A propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) Obtém um valor que indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a>Parâmetros

*bstrItem*

Um System. String que é um dos valores a seguir.



| Valor      | Descrição                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| voltar       | Descobre se o método **IWMPDVD. back** está disponível.                                   |
| DVD        | Descobre se o DVD está carregado.                                                          |
| dvdDecoder | Descobre se o decodificador de DVD está instalado no sistema.                                     |
| resume     | Descobre se o método **IWMPDVD. resume** está disponível.                                 |
| titleMenu  | Descobre se o método **IWMPDVD. titleMenu** está disponível.                              |
| topMenu    | Descobre se o método **IWMPDVD. topMenu** está disponível. Normalmente chamado de menu raiz. |



 

## <a name="property-value"></a>Valor da propriedade

**System.Boolean**

Um **System. Boolean** que indica se um tipo especificado de informações está disponível ou se uma ação especificada pode ser executada.

## <a name="remarks"></a>Comentários

os recursos de dvd do Windows Media Player não funcionarão em computadores que não têm um decodificador de DVD instalado. Você pode determinar se um decodificador está disponível chamando a propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) e passando o valor de **System. String** "dvdDecoder".

Cada DVD é criado de maneira diferente. Os métodos disponíveis durante a reprodução e navegação em DVD dependem de como o DVD é criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPDVD (VB e C#)**](iwmpdvd--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. Back (VB e C#)**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. resume (VB e C#)**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. titleMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[**IWMPDVD. topMenu (VB e C#)**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





