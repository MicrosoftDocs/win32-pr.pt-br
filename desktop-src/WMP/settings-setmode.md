---
title: método Configurações. setmode
description: O método setmode define vários modos como ativo ou inativo.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- método setmode Windows Media Player
- método setmode Windows Media Player, classe Configurações
- classe Configurações Windows Media Player, método setmode
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
ms.openlocfilehash: f504fe429dddf1b3db191545e2f34a3605a8fc390346c8f00afe8c3d005f0277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995316"
---
# <a name="settingssetmode-method"></a>método Configurações. setmode

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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando o modo de conquadro é ativo, o Player deve acessar o conteúdo da faixa para recuperar o quadro de vídeo. Devido a considerações de largura de banda, use esse modo com cuidado ao reproduzir conteúdo não local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | para modos de loop e ordem aleatória, Windows Media Player versão 7,0 ou posterior. para modos de autoretrocesso e de conquadro, Windows Media Player 9 Series ou posterior.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> <dt>

[**Configurações. getmode**](settings-getmode.md)
</dt> </dl>

 

 





