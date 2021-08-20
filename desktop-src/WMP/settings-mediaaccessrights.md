---
title: Configurações. mediaAccessRights
description: A propriedade mediaAccessRights recupera um valor que indica os direitos concedidos atualmente para acesso à biblioteca.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Configurações. mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b78543adcdc36958c6fb2f8e4ea191156bd8c600112e4bd6e5d6e6f5427974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933656"
---
# <a name="settingsmediaaccessrights"></a>Configurações. mediaAccessRights

A propriedade **mediaAccessRights** recupera um valor que indica os direitos concedidos atualmente para acesso à biblioteca.

## <a name="syntax"></a>Syntax

Player. Settings. mediaAccessRights

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.



| Valor | Descrição                      |
|-------|----------------------------------|
| nenhum  | Somente direitos de acesso do item atual. |
| ler  | Somente direitos de acesso de leitura.         |
| completa  | Direitos de acesso de leitura/gravação.        |



 

## <a name="remarks"></a>Comentários

Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca. Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos. para obter direitos de acesso, o aplicativo chama *Configurações*. **requestMediaAccessRights**, passando um parâmetro que especifica o nível de direitos de acesso desejado.

**Windows Media Player 10 Mobile**: essa propriedade sempre retorna **full**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





