---
title: Interface IWMPControls3 (VB e C) (Wmp.h)
description: Fornece propriedades e métodos para seleção de linguagem de áudio e suporte que complementam a interface IWMPControls2. Além das propriedades e métodos herdados de IWMPControls2, a interface IWMPControls3 expõe as propriedades a seguir.
ms.assetid: 1f42a352-da97-4382-9b59-a9b074aa2a5a
keywords:
- Interface IWMPControls3 (VB e C) Windows Media Player
- Interface IWMPControls3 (VB e C ) Windows Media Player , descrita
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
ms.openlocfilehash: 2baf3f0b5f2bc4f2e4d0bfa5ccddd717c913aa30f5e24b5559eb527c910bcaf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135409"
---
# <a name="iwmpcontrols3-vb-and-c-interface"></a>Interface IWMPControls3 (VB e C#)

Fornece propriedades e métodos para seleção de linguagem de áudio e suporte que complementam a interface **IWMPControls2.**

Além das propriedades e métodos herdados de **IWMPControls2,** a interface **IWMPControls3** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPControls3 (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPControls3 (VB e C#)** tem esses métodos.



| Método                                                                                                         | Descrição                                                                                               |
|:---------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**getAudioLanguageDescription**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md) | Retorna a descrição da linguagem de áudio correspondente ao índice baseado em um especificado.<br/> |
| [**getAudioLanguageID**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)                   | Retorna o LCID para um índice de linguagem de áudio especificado.<br/>                                         |
| [**getLanguageName**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)                         | Retorna o nome da linguagem de áudio com o LCID especificado.<br/>                                |



 

### <a name="properties"></a>Propriedades

A interface **IWMPControls3 (VB e C#)** tem essas propriedades.



| Propriedade                                                                                                              | Tipo de acesso           | Descrição                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**audioLanguageCount**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)<br/>               | Somente leitura<br/>  | Obtém a contagem de linguagens de áudio com suporte. <br/>                                                                                            |
| [**currentAudioLanguage**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)<br/>           | Leitura/gravação<br/> | Obtém ou define o LCID (identificador de localidade) da linguagem de áudio para reprodução. <br/>                                                           |
| [**currentAudioLanguageIndex**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)<br/> | Leitura/gravação<br/> | Obtém ou define o índice baseado em um que corresponde à linguagem de áudio para reprodução. <br/>                                                   |
| [**currentPositionTimecode**](wmplibiwmpcontrols3-iwmpcontrols3-currentpositiontimecode--vb-and-c.md)<br/>     | Leitura/gravação<br/> | Obtém ou define a posição atual no item de mídia atual usando um formato de código de hora. Atualmente, essa propriedade dá suporte ao código de hora SMPTE. <br/> |



 

Obter uma interface **IWMPControls3,** lançando o valor retornado pela propriedade [**AxWindowsMediaPlayer.Ctlcontrols.**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPControls (VB e C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Interface IWMPControls2 (VB e C#)**](iwmpcontrols2--vb-and-c.md)
</dt> </dl>

 

 





