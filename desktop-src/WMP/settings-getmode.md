---
title: Método Settings. GetMode
description: O método GetMode determina se o modo de loop ou de ordem aleatória está ativo.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- método GetMode do Windows Media Player
- método GetMode Windows Media Player, classe Settings
- Classe de configurações Windows Media Player, método GetMode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748093"
---
# <a name="settingsgetmode-method"></a>Método Settings. GetMode

O método **GetMode** determina se o modo de loop ou de ordem aleatória está ativo.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*modeName* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do modo em questão, contendo um dos valores a seguir.



| String     | Descrição                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| rebobinar | As faixas são reiniciadas no início depois da reprodução até o fim.                                                          |
| loop       | A sequência de faixas se repete.                                                                                   |
| conmoldura  | O quadro de chave mais próximo é exibido na posição atual quando não está sendo executado. Esse modo não é relevante para faixas de áudio. |
| ordem aleatória    | As faixas são reproduzidas em ordem aleatória.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um valor **booliano** que indica se o modo especificado está ativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Para modos de loop e ordem aleatória, Windows Media Player versão 7,0 ou posterior. Para modos de autoretrocesso e de conframe, o Windows Media Player 9 Series ou posterior.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> <dt>

[**Settings. setmode**](settings-setmode.md)
</dt> </dl>

 

 





