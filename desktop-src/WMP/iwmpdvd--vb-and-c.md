---
title: Interface IWMPDVD (VB e C) (WMP. h)
description: A interface IWMPDVD fornece propriedades e métodos para trabalhar com DVDs. a interface IWMPDVD expõe as propriedades a seguir.
ms.assetid: 6bb32eed-475e-4867-8318-34578dc430a4
keywords:
- IWMPDVD (VB e C) interface do Windows Media Player
- IWMPDVD (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPDVD (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425c048096ad7cd65e0e48ccf2932f00a817d790
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762066"
---
# <a name="iwmpdvd-vb-and-c-interface"></a>Interface IWMPDVD (VB e C#)

A interface **IWMPDVD** fornece propriedades e métodos para trabalhar com DVDs.

A interface **IWMPDVD** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPDVD (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPDVD (VB e C#)** tem esses métodos.



| Método                                                         | Descrição                                                                                                     |
|:---------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Voltar**](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)           | Altera a exibição de um submenu para seu menu pai.<br/>                                               |
| [**Volte**](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)       | Altera para o modo de reprodução no modo de menu, retomando na mesma posição em que o menu foi invocado.<br/> |
| [**titleMenu**](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md) | Interrompe a reprodução e exibe o menu de título.<br/>                                                          |
| [**topMenu**](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)     | Interrompe a reprodução e exibe o menu raiz.<br/>                                                           |



 

### <a name="properties"></a>Propriedades

A interface **IWMPDVD (VB e C#)** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso          | Descrição                                                                                                                                                                          |
|:--------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**controlador**](wmplibiwmpdvd-iwmpdvd-domain--vb-and-c.md)<br/> | Somente leitura<br/> | Obtém o domínio atual do DVD.<br/>                                                                                                                                       |
| [**isAvailable**](iwmpdvd-isavailable--vb-and-c.md)<br/>     | Somente leitura<br/> | Obtém um valor que indica se um tipo de informação especificado está disponível ou se uma ação especificada pode ser executada. No C#, esse é o método **Get \_ IsAvailable** .<br/> |



 

Obtenha uma interface **IWMPDVD** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**DVD**](axwmplib-axwindowsmediaplayer-dvd--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





