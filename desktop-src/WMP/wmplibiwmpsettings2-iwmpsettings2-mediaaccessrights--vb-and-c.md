---
title: Propriedade IWMPSettings2 mediaAccessRights
description: A propriedade mediaAccessRights obtém um valor que indica as permissões atualmente concedidas para acesso à biblioteca.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- propriedade mediaAccessRights Windows Media Player
- propriedade mediaAccessRights Windows Media Player interface , IWMPSettings2
- Interface IWMPSettings2 Windows Media Player , propriedade mediaAccessRights
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
ms.openlocfilehash: 797e45c62b505033afd2126f79d5830de5bc9847a4de36199a6c919a4978f112
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122486"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>Propriedade IWMPSettings2::mediaAccessRights

A **propriedade mediaAccessRights** obtém um valor que indica as permissões atualmente concedidas para acesso à biblioteca.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System.String** que é um dos valores a seguir.



| Valor | Descrição                      |
|-------|----------------------------------|
| nenhum  | Somente direitos de acesso de item atual. |
| ler  | Somente direitos de acesso de leitura.         |
| completa  | Direitos de acesso de leitura/gravação.        |



 

## <a name="remarks"></a>Comentários

Uma página da Web deve primeiro solicitar permissão do usuário para ler informações ou gravar dados na biblioteca. Isso significa que determinados métodos, propriedades e eventos estarão inacessíveis do código se os direitos de acesso apropriados não foram concedidos. Para obter direitos de acesso, o aplicativo chama **IWMPSettings2.get \_ requestMediaAccessRights**, passando um parâmetro que especifica o nível de direitos de acesso desejado.

Os aplicativos em execução no computador do usuário sempre têm direitos de acesso completo.

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

[**IWMPSettings2.requestMediaAccessRights (VB e C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





