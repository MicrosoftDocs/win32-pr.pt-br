---
title: Método Settings. setmode
description: O método setmode define vários modos como ativo ou inativo.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- método setmode do Windows Media Player
- método setmode Windows Media Player, classe Settings
- Classe de configurações Windows Media Player, método setmode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747495"
---
# <a name="settingssetmode-method"></a>Método Settings. setmode

O método **setmode** define vários modos como ativo ou inativo.

## <a name="syntax"></a>Sintaxe


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*modeName* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nome do modo que está sendo alterado, contendo um dos valores a seguir.



| String     | Descrição                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| rebobinar | Modo que indica se as faixas são rebobinadas para o início após a reprodução até o fim. O estado padrão é true.                                                  |
| loop       | Modo que indica se a sequência de faixas se repete. O estado padrão é false.                                                                            |
| conmoldura  | Modo que indica se o quadro de chave de vídeo mais próximo é exibido na posição atual quando não está sendo executado. O estado padrão é false. Não tem nenhum efeito nas faixas de áudio. |
| ordem aleatória    | Modo que indica se as faixas são reproduzidas em ordem aleatória. O estado padrão é false.                                                                            |



 

</dd> <dt>

*estado* \[ no\]
</dt> <dd>

**Booliano** que especifica se o novo modo especificado está ativo ou não.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando o modo de conquadro é ativo, o Player deve acessar o conteúdo da faixa para recuperar o quadro de vídeo. Devido a considerações de largura de banda, use esse modo com cuidado ao reproduzir conteúdo não local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Para modos de loop e ordem aleatória, Windows Media Player versão 7,0 ou posterior. Para modos de autoretrocesso e de conframe, o Windows Media Player 9 Series ou posterior.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> <dt>

[**Settings. GetMode**](settings-getmode.md)
</dt> </dl>

 

 





