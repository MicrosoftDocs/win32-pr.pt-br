---
title: Interface IWMPSettings (VB e C) (WMP. h)
description: Fornece propriedades e métodos que obtêm ou definem os valores das configurações do Windows Media Player. A interface IWMPSettings expõe as propriedades a seguir.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- IWMPSettings (VB e C) interface do Windows Media Player
- IWMPSettings (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPSettings (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db911cc6d18ba40777e77a803480c7fcab4ff8ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761010"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>Interface IWMPSettings (VB e C#)

Fornece propriedades e métodos que obtêm ou definem os valores das configurações do Windows Media Player.

A interface **IWMPSettings** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPSettings (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPSettings (VB e C#)** tem esses métodos.



| Método                                                               | Descrição                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**GetMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Retorna um valor indicando se o modo de loop ou o modo de ordem aleatória está ativo.<br/> |
| [**setmode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Define o modo de loop ou de ordem aleatória como ativo ou inativo.<br/>               |



 

### <a name="properties"></a>Propriedades

A interface **IWMPSettings (VB e C#)** tem essas propriedades.



| Propriedade                                                                                              | Tipo de acesso           | Descrição                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inicialização automática**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define um valor que indica se o item de mídia atual começa a ser reproduzido automaticamente. <br/>                                     |
| [**Lance**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define o saldo do estéreo atual.<br/>                                                                                          |
| [**baseURL**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos no conteúdo de mídia digital. <br/> |
| [**DefaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Leitura/gravação<br/> | Obtém ou define o nome do quadro usado para exibir uma URL recebida em um evento **scriptCommand** . <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor que indica se as caixas de diálogo de erro são exibidas automaticamente.<br/>                                           |
| [**invokeURLs**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define um valor que indica se os eventos de URL devem iniciar um navegador da Web. <br/>                                                  |
| [**isAvailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Somente leitura<br/>  | Obtém um valor que indica se uma ação especificada pode ser executada. No C#, esse é o método **Get \_ IsAvailable** .<br/>             |
| [**Muta**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Leitura/gravação<br/> | Obtém ou define um valor que indica se o áudio está mudo. <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define o número de vezes que um item de mídia será reproduzido. <br/>                                                                         |
| [**frequência**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Leitura/gravação<br/> | Obtém ou define a taxa de reprodução atual para vídeo. <br/>                                                                                |
| [**volume**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define o volume de reprodução atual. <br/>                                                                                        |



 

Obtenha uma interface **IWMPSettings** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Configurações**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





