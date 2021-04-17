---
title: Interface IWMPSettings2 (VB e C) (WMP. h)
description: Fornece propriedades e um método que complementam a interface IWMPSettings. Além das propriedades e métodos herdados de IWMPSettings, a interface IWMPSettings2 expõe as propriedades a seguir.
ms.assetid: 6bd0f6dd-df49-4c21-b47c-c8c63f85c2c0
keywords:
- IWMPSettings2 (VB e C) interface do Windows Media Player
- IWMPSettings2 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPSettings2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb782433085544a94db0eab6b9314f1e4df488e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797563"
---
# <a name="iwmpsettings2-vb-and-c-interface"></a>Interface IWMPSettings2 (VB e C#)

Fornece propriedades e um método que complementam a interface **IWMPSettings** .

Além das propriedades e métodos herdados de **IWMPSettings**, a interface **IWMPSettings2** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPSettings2 (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPSettings2 (VB e C#)** tem esses métodos.



| Método                                                                                                   | Descrição                                                     |
|:---------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**requestMediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md) | Solicita um nível especificado de acesso à biblioteca.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IWMPSettings2 (VB e C#)** tem essas propriedades.



| Propriedade                                                                                                    | Tipo de acesso          | Descrição                                                                               |
|:------------------------------------------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [**defaultAudioLanguage**](wmplibiwmpsettings2-iwmpsettings2-defaultaudiolanguage--vb-and-c.md)<br/> | Somente leitura<br/> | Obtém o LCID (identificador de localidade) do idioma de áudio padrão. <br/>              |
| [**mediaAccessRights**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)<br/>       | Somente leitura<br/> | Obtém um valor que indica as permissões concedidas atualmente para acesso à biblioteca. <br/> |



 

Obtenha uma interface **IWMPSettings2** convertendo o valor retornado pela propriedade **AxWindowsMediaPlayer. Settings** .



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

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





