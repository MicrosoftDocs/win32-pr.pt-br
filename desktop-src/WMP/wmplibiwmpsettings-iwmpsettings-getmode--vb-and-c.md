---
title: Método getMode IWMPSettings
description: O método getMode retorna um valor que indica se o modo de loop ou modo de embaralhamento está ativo.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- Método getMode Windows Media Player
- Método getMode Windows Media Player interface , IWMPSettings
- Interface IWMPSettings Windows Media Player , método getMode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae5d910dbbdf1fc2241a63dcf6c61c94e968cf0f2b36316407aafc8fc5f2dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246296"
---
# <a name="iwmpsettingsgetmode-method"></a>Método IWMPSettings::getMode

O **método getMode** retorna um valor que indica se o modo de loop ou modo de embaralhamento está ativo.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrMode* \[ Em\]
</dt> <dd>

Um **System.String** que é um dos valores a seguir.



| Valor      | Descrição                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | As faixas são reiniciadas desde o início após a reprodução até o final.                                |
| loop       | A sequência de faixas se repete.                                                           |
| showFrame  | O quadro-chave mais próximo é exibido quando não está em reprodução. Esse modo não é relevante para faixas de áudio. |
| ordem aleatória    | As faixas são tocadas em ordem aleatória.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **valor System.Boolean** que indica se o modo especificado está ativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.setMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





