---
title: Método IWMPClosedCaption2 getSAMIStyleName
description: O método getSAMIStyleName retorna o nome de um estilo suportado pelo arquivo SAMI atual.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- método getSAMIStyleName Windows Media Player
- método getSAMIStyleName Windows Media Player, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player, método getSAMIStyleName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782871"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>Método IWMPClosedCaption2:: getSAMIStyleName

O método **getSAMIStyleName** retorna o nome de um estilo suportado pelo arquivo Sami atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nIndex* \[ no\]
</dt> <dd>

Um **System. Int32** que é o índice de base zero do nome do estilo a ser recuperado

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. String** que é o nome do estilo, conforme especificado no arquivo Sami.

## <a name="remarks"></a>Comentários

Os estilos em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.

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

[**IWMPClosedCaption. SAMIstyle (VB e C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





