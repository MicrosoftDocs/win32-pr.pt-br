---
title: método Configurações.requestMediaAccessRights
description: O método requestMediaAccessRights solicita um nível especificado de acesso à biblioteca. | Configurações.requestMediaAccessRights
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- Método requestMediaAccessRights Windows Media Player
- Método requestMediaAccessRights Windows Media Player , Configurações classe
- Configurações classe Windows Media Player , método requestMediaAccessRights
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
ms.openlocfilehash: 1e157e7b4495c8d90964d62a9045eebb202126906f0022e97c4983220e47ac03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569307"
---
# <a name="settingsrequestmediaaccessrights-method"></a>método Configurações.requestMediaAccessRights

O **método requestMediaAccessRights** solicita um nível especificado de acesso à biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*acesso* \[ Em\]
</dt> <dd>

**Cadeia de** caracteres que especifica o nível de direitos de acesso desejado. Contém um dos seguintes valores.



| String | Descrição                      |
|--------|----------------------------------|
| nenhum   | Somente direitos de acesso de item atual. |
| ler   | Somente direitos de acesso de leitura.         |
| completa   | Direitos de acesso de leitura/gravação.        |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **valor booliana** que indica se os direitos de acesso solicitados foram concedidos.

## <a name="remarks"></a>Comentários

Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca. Invocar esse método solicita ao usuário uma caixa de diálogo que solicita o nível de permissão especificado. Isso significa que determinados métodos, propriedades e eventos estarão inacessíveis do código se os direitos de acesso apropriados não foram concedidos. O nível de direitos de acesso atual pode ser recuperado usando *Configurações*. **mediaAccessRights**.

**Windows Media Player 10 Mobile:** esse método sempre retorna **true.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





