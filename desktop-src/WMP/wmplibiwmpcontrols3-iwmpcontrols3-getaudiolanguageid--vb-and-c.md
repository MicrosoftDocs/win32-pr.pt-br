---
title: Método IWMPControls3 getAudioLanguageID
description: O método getAudioLanguageID retorna o LCID (identificador de localidade) para um índice de idioma de áudio especificado.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- método getAudioLanguageID Windows Media Player
- método getAudioLanguageID Windows Media Player, interface IWMPControls3
- Interface IWMPControls3 Windows Media Player, método getAudioLanguageID
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750110"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a>Método IWMPControls3:: getAudioLanguageID

O método **getAudioLanguageID** retorna o LCID (identificador de localidade) para um índice de idioma de áudio especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Lindex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice baseado em um do idioma de áudio.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. Int32** que é o LCID.

## <a name="remarks"></a>Comentários

Um LCID identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

Para conteúdo baseado no Windows, as propriedades e os métodos relacionados à seleção de idioma dão suporte a apenas uma única saída.

Use a propriedade **audioLanguageCount** para obter o número de idiomas de áudio com suporte e, em seguida, acesse um idioma de áudio individualmente usando um índice com base em um.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPControls3 (VB e C#)**](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. audioLanguageCount (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. currentAudioLanguageIndex (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getAudioLanguageDescription (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[**IWMPControls3. getLanguageName (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





