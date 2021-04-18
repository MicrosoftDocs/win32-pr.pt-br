---
title: Método IWMPClosedCaption2 getSAMILangName
description: O método getSAMILangName retorna o nome de um idioma com suporte do arquivo SAMI atual.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- método getSAMILangName Windows Media Player
- método getSAMILangName Windows Media Player, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player, método getSAMILangName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788018"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>Método IWMPClosedCaption2:: getSAMILangName

O método **getSAMILangName** retorna o nome de um idioma com suporte do arquivo Sami atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nIndex* \[ no\]
</dt> <dd>

**Um System. Int32** que é o índice de base zero do nome do idioma a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. String** que é o nome do idioma conforme especificado no arquivo Sami.

## <a name="remarks"></a>Comentários

Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.

Esse método retorna uma cadeia de caracteres de comprimento zero (""), a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer. OpenState é igual a 13).

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

[**IWMPClosedCaption. SAMILang (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





