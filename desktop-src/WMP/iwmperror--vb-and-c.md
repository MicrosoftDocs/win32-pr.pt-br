---
title: Interface IWMPError (VB e C) (WMP. h)
description: Fornece propriedades e métodos para acessar uma coleção de interfaces IWMPErrorItem para recuperar informações de erro. A interface IWMPError expõe as propriedades a seguir.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- Windows Media Player de interface IWMPError (VB e C)
- Windows Media Player de interface IWMPError (VB e C), descrita
topic_type:
- apiref
api_name:
- IWMPError (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f3ff7635e423d70447e371d61fbbadf02aa14c2476e118be79cbb25d974348b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736176"
---
# <a name="iwmperror-vb-and-c-interface"></a>Interface IWMPError (VB e C#)

Fornece propriedades e métodos para acessar uma coleção de interfaces **IWMPErrorItem** para recuperar informações de erro.

A interface **IWMPError** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPError (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPError (VB e C#)** tem esses métodos.



| Método                                                                         | Descrição                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearErrorQueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | Limpa os erros da fila de erros.<br/>                                                                                            |
| [**Webhelp**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | inicia a página de ajuda da Web do Microsoft Windows Media Player para exibir mais informações sobre o primeiro erro na fila de erros.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IWMPError (VB e C#)** tem essas propriedades.



| Propriedade                                                                        | Tipo de acesso           | Descrição                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | Somente leitura<br/>  | Obtém o número de erros na fila de erros.<br/>                                                                            |
| [**Item**](iwmperror-item--vb-and-c.md)<br/>                             | Leitura/gravação<br/> | Obtém uma interface **IWMPErrorItem** no índice especificado na fila de erros. No C#, esse é o método **Get \_ Item** .<br/> |



 

Obtenha uma interface **IWMPError** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Erro**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .net e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPErrorItem (VB e C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





