---
title: Método GetMode IWMPSettings
description: O método GetMode retorna um valor que indica se o modo de loop ou o modo de ordem aleatória está ativo.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- método GetMode do Windows Media Player
- método GetMode Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, método GetMode
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
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814446"
---
# <a name="iwmpsettingsgetmode-method"></a>Método IWMPSettings:: GetMode

O método **GetMode** retorna um valor que indica se o modo de loop ou o modo de ordem aleatória está ativo.

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

*bstrmode* \[ no\]
</dt> <dd>

Um **System. String** que é um dos valores a seguir.



| Valor      | Descrição                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| rebobinar | As faixas são reiniciadas desde o início após a execução até o final.                                |
| loop       | A sequência de faixas se repete.                                                           |
| conmoldura  | O quadro de chave mais próximo é exibido quando não está sendo executado. Esse modo não é relevante para faixas de áudio. |
| ordem aleatória    | As faixas são reproduzidas em ordem aleatória.                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um valor **System. booliano** que indica se o modo especificado está ativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





