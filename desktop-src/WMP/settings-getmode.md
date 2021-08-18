---
title: método Configurações.getMode
description: O método getMode determina se o modo de loop ou modo de embaralhamento está ativo.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- Método getMode Windows Media Player
- Método getMode Windows Media Player classe Configurações ,
- Configurações classe Windows Media Player , método getMode
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
ms.openlocfilehash: 779c775319cbe0d6dc443b4eb99febd494db3d30fb35228b7310f8f1ae7d691d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995326"
---
# <a name="settingsgetmode-method"></a>método Configurações.getMode

O **método getMode** determina se o modo de loop ou modo de embaralhamento está ativo.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*modeName* \[ Em\]
</dt> <dd>

**Cadeia** de caracteres que especifica o nome do modo em questão, contendo um dos valores a seguir.



| String     | Descrição                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| autoRewind | As faixas são reiniciadas no início após a reprodução até o final.                                                          |
| loop       | A sequência de faixas se repete.                                                                                   |
| showFrame  | O quadro-chave mais próximo é exibido na posição atual quando não está em reprodução. Esse modo não é relevante para faixas de áudio. |
| ordem aleatória    | As faixas são tocadas em ordem aleatória.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **valor booliana** que indica se o modo especificado está ativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Para modos de loop e embaralhamento, Windows Media Player versão 7.0 ou posterior. Para os modos autoRewind e showFrame, Windows Media Player Série 9 ou posterior.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> <dt>

[**Configurações.setMode**](settings-setmode.md)
</dt> </dl>

 

 





