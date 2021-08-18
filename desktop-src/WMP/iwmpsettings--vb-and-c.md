---
title: Interface IWMPSettings (VB e C ) (Wmp.h)
description: Fornece propriedades e métodos que obterão ou definirão os valores de Windows Media Player configurações. A interface IWMPSettings expõe as propriedades a seguir.
ms.assetid: fb37b455-221e-4cee-a219-cacf2938a92a
keywords:
- Interface IWMPSettings (VB e C) Windows Media Player
- Interface IWMPSettings (VB e C ) Windows Media Player , descrita
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
ms.openlocfilehash: 6a537efcd9b39f993705244020e579b9d667164180fd5cd70ab05fc692bed8fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996466"
---
# <a name="iwmpsettings-vb-and-c-interface"></a>Interface IWMPSettings (VB e C#)

Fornece propriedades e métodos que obterão ou definirão os valores de Windows Media Player configurações.

A interface **IWMPSettings** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPSettings (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPSettings (VB e C#)** tem esses métodos.



| Método                                                               | Descrição                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**getMode**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md) | Retorna um valor que indica se o modo de loop ou modo de embaralhamento está ativo.<br/> |
| [**setMode**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md) | Define o modo de loop ou modo de embaralhamento como ativo ou inativo.<br/>               |



 

### <a name="properties"></a>Propriedades

A interface **IWMPSettings (VB e C#)** tem essas propriedades.



| Propriedade                                                                                              | Tipo de acesso           | Descrição                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autostart**](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define um valor que indica se o item de mídia atual começa a ser a reprodução automática. <br/>                                     |
| [**Equilíbrio**](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define o saldo estéreo atual.<br/>                                                                                          |
| [**Baseurl**](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)<br/>                       | Leitura/gravação<br/> | Obtém ou define a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos no conteúdo de mídia digital. <br/> |
| [**defaultFrame**](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)<br/>             | Leitura/gravação<br/> | Obtém ou define o nome do quadro usado para exibir uma URL recebida em um **evento scriptCommand.** <br/>                          |
| [**enableErrorDialogs**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor que indica se as caixas de diálogo de erro são exibidas automaticamente.<br/>                                           |
| [**Invokeurls**](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)<br/>                 | Leitura/gravação<br/> | Obtém ou define um valor que indica se os eventos de URL devem iniciar um navegador da Web. <br/>                                                  |
| [**Isavailable**](iwmpsettings-isavailable--vb-and-c.md)<br/>                                  | Somente leitura<br/>  | Obtém um valor que indica se uma ação especificada pode ser executada. Em C#, esse é o **método \_ get isAvailable.**<br/>             |
| [**Mudo**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)<br/>                             | Leitura/gravação<br/> | Obtém ou define um valor que indica se o áudio é mudo. <br/>                                                                          |
| [**playCount**](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define o número de vezes que um item de mídia será reproduzir. <br/>                                                                         |
| [**Taxa**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)<br/>                             | Leitura/gravação<br/> | Obtém ou define a taxa de reprodução atual para vídeo. <br/>                                                                                |
| [**Volume**](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)<br/>                         | Leitura/gravação<br/> | Obtém ou define o volume de reprodução atual. <br/>                                                                                        |



 

Obter uma **interface IWMPSettings** usando a propriedade a seguir.



| Objeto                                                                   | Propriedade                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Configurações**](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





