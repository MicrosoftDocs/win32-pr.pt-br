---
title: Método setmode IWMPSettings
description: O método setmode define o modo de loop ou de ordem aleatória como ativo ou inativo.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- método setmode do Windows Media Player
- método setmode Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, método setmode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764169"
---
# <a name="iwmpsettingssetmode-method"></a>Método IWMPSettings:: setmode

O método **setmode** define o modo de loop ou de ordem aleatória como ativo ou inativo.

## <a name="syntax"></a>Sintaxe


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrmode* \[ no\]
</dt> <dd>

Um **System. String** que é o nome do modo que está sendo alterado, contendo um dos valores a seguir.



| Valor      | Descrição                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| rebobinar | As faixas são reiniciadas desde o início após a execução até o final.                                |
| loop       | A sequência de faixas se repete.                                                           |
| conmoldura  | O quadro de chave mais próximo é exibido quando não está sendo executado. Esse modo não é relevante para faixas de áudio. |
| ordem aleatória    | As faixas são reproduzidas em ordem aleatória.                                                               |



 

</dd> <dt>

*varfMode* \[ no\]
</dt> <dd>

Um valor **System. Boolean** que especifica se o novo modo especificado está ativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando o modo de conmoldura está ativo, o Windows Media Player deve acessar o conteúdo de acompanhamento para recuperar o quadro de vídeo. Use esse modo com cuidado ao reproduzir conteúdo que não seja local.

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

[**IWMPSettings. GetMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





