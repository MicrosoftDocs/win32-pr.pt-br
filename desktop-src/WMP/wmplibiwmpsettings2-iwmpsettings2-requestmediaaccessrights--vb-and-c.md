---
title: Método IWMPSettings2 requestMediaAccessRights
description: O método requestMediaAccessRights solicita um nível especificado de acesso à biblioteca. | Método IWMPSettings2 requestMediaAccessRights
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- Método requestMediaAccessRights Windows Media Player
- Método requestMediaAccessRights Windows Media Player interface , IWMPSettings2
- Interface IWMPSettings2 Windows Media Player , método requestMediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba44540717059945f273be23d2e3c63b3c10cfc6d21d35ee1c4756ea1503708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568483"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>Método IWMPSettings2::requestMediaAccessRights

O **método requestMediaAccessRights** solicita um nível especificado de acesso à biblioteca.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrDesiredAccess* \[ Em\]
</dt> <dd>

Um **System.String** que é um dos valores a seguir.



| Valor | Descrição                      |
|-------|----------------------------------|
| nenhum  | Somente direitos de acesso de item atual. |
| ler  | Somente direitos de acesso de leitura.         |
| completa  | Direitos de acesso de leitura/gravação.        |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.Boolean** que indica se os direitos de acesso solicitados foram concedidos.

## <a name="remarks"></a>Comentários

Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca. Invocar esse método solicita ao usuário uma caixa de diálogo que solicita o nível de permissão especificado. Isso significa que determinados métodos, propriedades e eventos estarão inacessíveis do código se os direitos de acesso apropriados não foram concedidos. O nível de direitos de acesso atual pode ser recuperado usando **IWMPSettings2.mediaAccessRights**.

Os aplicativos em execução no computador do usuário não são necessários para usar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





