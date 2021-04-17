---
title: Propriedade IWMPSettings2 mediaAccessRights
description: A propriedade mediaAccessRights Obtém um valor que indica as permissões concedidas atualmente para acesso à biblioteca.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Propriedade mediaAccessRights Windows Media Player
- Propriedade mediaAccessRights Windows Media Player, interface IWMPSettings2
- Interface IWMPSettings2 Windows Media Player, Propriedade mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768813"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>Propriedade IWMPSettings2:: mediaAccessRights

A propriedade **mediaAccessRights** Obtém um valor que indica as permissões concedidas atualmente para acesso à biblioteca.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é um dos valores a seguir.



| Valor | Descrição                      |
|-------|----------------------------------|
| nenhum  | Somente direitos de acesso do item atual. |
| ler  | Somente direitos de acesso de leitura.         |
| completa  | Direitos de acesso de leitura/gravação.        |



 

## <a name="remarks"></a>Comentários

Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca. Isso significa que determinados métodos, propriedades e eventos ficarão inacessíveis a partir do código se os direitos de acesso apropriados não tiverem sido concedidos. Para obter direitos de acesso, o aplicativo chama **IWMPSettings2. get \_ requestMediaAccessRights**, passando um parâmetro que especifica o nível de direitos de acesso desejado.

Os aplicativos em execução no computador do usuário sempre têm direitos de acesso total.

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

[**IWMPSettings2. requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





