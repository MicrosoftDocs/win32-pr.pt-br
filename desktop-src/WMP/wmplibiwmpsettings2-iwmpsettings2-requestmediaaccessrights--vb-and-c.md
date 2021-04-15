---
title: Método IWMPSettings2 requestMediaAccessRights
description: O método requestMediaAccessRights solicita um nível especificado de acesso à biblioteca. | Método IWMPSettings2 requestMediaAccessRights
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- método requestMediaAccessRights Windows Media Player
- método requestMediaAccessRights Windows Media Player, interface IWMPSettings2
- Interface IWMPSettings2 Windows Media Player, método requestMediaAccessRights
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
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761315"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>Método IWMPSettings2:: requestMediaAccessRights

O método **requestMediaAccessRights** solicita um nível especificado de acesso à biblioteca.

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

*bstrDesiredAccess* \[ no\]
</dt> <dd>

Um **System. String** que é um dos valores a seguir.



| Valor | Descrição                      |
|-------|----------------------------------|
| none  | Somente direitos de acesso do item atual. |
| ler  | Somente direitos de acesso de leitura.         |
| completa  | Direitos de acesso de leitura/gravação.        |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. Boolean** que indica se os direitos de acesso solicitados foram concedidos.

## <a name="remarks"></a>Comentários

Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca. Invocar esse método solicita ao usuário uma caixa de diálogo que solicita o nível de permissão especificado. Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos. O nível de direitos de acesso atual pode ser recuperado usando **IWMPSettings2. mediaAccessRights**.

Os aplicativos em execução no computador do usuário não são obrigados a usar esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPSettings2 (VB e C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





