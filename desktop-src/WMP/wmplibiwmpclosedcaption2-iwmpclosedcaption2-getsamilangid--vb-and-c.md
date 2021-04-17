---
title: Método IWMPClosedCaption2 getSAMILangID
description: O método getSAMILangID retorna o LCID (identificador de localidade) de um idioma com suporte do arquivo SAMI atual.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- método getSAMILangID Windows Media Player
- método getSAMILangID Windows Media Player, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player, método getSAMILangID
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759930"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>Método IWMPClosedCaption2:: getSAMILangID

O método **getSAMILangID** retorna o LCID (identificador de localidade) de um idioma com suporte do arquivo Sami atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nIndex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice de base zero do LCID a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. Int32** que é o LCID do idioma com o índice especificado.

## <a name="remarks"></a>Comentários

Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.

Esse método retorna 0, a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer. OpenState é igual a 13).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





