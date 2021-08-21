---
title: Método IWMPClosedCaption2 getSAMILangID
description: O método getSAMILangID retorna o LCID (identificador de localidade) de um idioma com suporte no arquivo SAMI atual.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- Método getSAMILangID Windows Media Player
- Método getSAMILangID Windows Media Player interface , IWMPClosedCaption2
- Interface IWMPClosedCaption2 Windows Media Player , método getSAMILangID
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
ms.openlocfilehash: a0fc62222f98d6c056bb8ce9ffd328582a6764202bb8446617471d3f7cb4a5ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506425"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a>Método IWMPClosedCaption2::getSAMILangID

O **método getSAMILangID** retorna o LCID (identificador de localidade) de um idioma com suporte no arquivo SAMI atual.

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

*nIndex* \[ Em\]
</dt> <dd>

Um **System.Int32 que** é o índice baseado em zero do LCID a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.Int32** que é o LCID da linguagem com o índice especificado.

## <a name="remarks"></a>Comentários

Os idiomas em um arquivo SAMI são indexados na ordem mostrada no arquivo, começando com zero.

Esse método retorna 0, a menos que um arquivo de mídia digital esteja aberto (AxWindowsMediaPlayer.openState é igual a 13).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





