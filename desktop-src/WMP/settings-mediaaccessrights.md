---
title: Settings. mediaAccessRights
description: A propriedade mediaAccessRights recupera um valor que indica os direitos concedidos atualmente para acesso à biblioteca.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Settings. mediaAccessRights Windows Media Player
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
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807325"
---
# <a name="settingsmediaaccessrights"></a>Settings. mediaAccessRights

A propriedade **mediaAccessRights** recupera um valor que indica os direitos concedidos atualmente para acesso à biblioteca.

## <a name="syntax"></a>Syntax

Player. Settings. mediaAccessRights

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.



| Valor | Descrição                      |
|-------|----------------------------------|
| none  | Somente direitos de acesso do item atual. |
| ler  | Somente direitos de acesso de leitura.         |
| completa  | Direitos de acesso de leitura/gravação.        |



 

## <a name="remarks"></a>Comentários

Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca. Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos. Para obter direitos de acesso, o aplicativo chama *as configurações*. **requestMediaAccessRights**, passando um parâmetro que especifica o nível de direitos de acesso desejado.

**Windows Media Player 10 Mobile**: essa propriedade sempre retorna **Full**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





