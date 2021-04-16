---
title: Método Settings. requestMediaAccessRights
description: O método requestMediaAccessRights solicita um nível especificado de acesso à biblioteca. | Método Settings. requestMediaAccessRights
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- método requestMediaAccessRights Windows Media Player
- método requestMediaAccessRights Windows Media Player, classe Settings
- Classe de configurações Windows Media Player, método requestMediaAccessRights
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747496"
---
# <a name="settingsrequestmediaaccessrights-method"></a>Método Settings. requestMediaAccessRights

O método **requestMediaAccessRights** solicita um nível especificado de acesso à biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*acesso* \[ ao no\]
</dt> <dd>

**Cadeia de caracteres** que especifica o nível de direitos de acesso desejado. Contém um dos seguintes valores.



| String | Descrição                      |
|--------|----------------------------------|
| none   | Somente direitos de acesso do item atual. |
| ler   | Somente direitos de acesso de leitura.         |
| completa   | Direitos de acesso de leitura/gravação.        |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um valor **booliano** que indica se os direitos de acesso solicitados foram concedidos.

## <a name="remarks"></a>Comentários

Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca. Invocar esse método solicita ao usuário uma caixa de diálogo que solicita o nível de permissão especificado. Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos. O nível de direitos de acesso atual pode ser recuperado usando *as configurações*. **mediaAccessRights**.

**Windows Media Player 10 Mobile**: esse método sempre retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





