---
title: Interface IWMPControls3 (VB e C) (WMP. h)
description: Fornece propriedades e métodos para seleção de idioma de áudio e suporte que complementam a interface IWMPControls2. Além das propriedades e métodos herdados de IWMPControls2, a interface IWMPControls3 expõe as propriedades a seguir.
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- IWMPControls3 (VB e C) interface do Windows Media Player
- IWMPControls3 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPControls3 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9788dbd1b5910d655cbaa17055c76a0ae6d0280e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763340"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>Interface IWMPControls3 (VB e C#)

Fornece propriedades e métodos para seleção de idioma de áudio e suporte que complementam a interface **IWMPControls2** .

Além das propriedades e métodos herdados de **IWMPControls2**, a interface **IWMPControls3** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPControls3 (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPControls3 (VB e C#)** tem esses métodos.



| Método                                                                                                         | Descrição                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**getAudioLanguageDescription**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | Retorna a descrição do idioma de áudio correspondente ao índice baseado em um especificado.<br/> |
| [**getAudioLanguageID**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | Retorna o LCID de um índice de idioma de áudio especificado.<br/>                                         |
| [**getLanguageName**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | Retorna o nome do idioma de áudio com o LCID especificado.<br/>                                |



 

### <a name="properties"></a>Propriedades

A interface **IWMPControls3 (VB e C#)** tem essas propriedades.



| Propriedade                                                                                                              | Tipo de acesso           | Descrição                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**audioLanguageCount**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | Somente leitura<br/>  | Obtém a contagem de idiomas de áudio com suporte. <br/>                                                                                            |
| [**currentAudioLanguage**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | Leitura/gravação<br/> | Obtém ou define o identificador de localidade (LCID) do idioma de áudio para reprodução. <br/>                                                           |
| [**currentAudioLanguageIndex**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | Leitura/gravação<br/> | Obtém ou define o índice com base em um que corresponde ao idioma de áudio para reprodução. <br/>                                                   |
| [**currentPositionTimecode**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | Leitura/gravação<br/> | Obtém ou define a posição atual no item de mídia atual usando um formato de código de tempo. Essa propriedade atualmente dá suporte ao código de tempo SMPTE. <br/> |



 

Obtenha uma interface **IWMPControls3** convertendo o valor retornado pela propriedade [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls2 (VB e C#)**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





