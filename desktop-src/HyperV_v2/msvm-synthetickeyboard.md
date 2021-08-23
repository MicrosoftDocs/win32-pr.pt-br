---
description: Representa um dispositivo de teclado sintético.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Msvm_SyntheticKeyboard classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ee3a7835349ab47082627f98020f84084b4b86e9c6b4ce4a37ba2f455497cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582216"
---
# <a name="msvm_synthetickeyboard-class"></a>Classe Msvm \_ SyntheticKeyboard

Representa um dispositivo de teclado sintético.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ SyntheticKeyboard** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **classe Msvm \_ SyntheticKeyboard** tem esses métodos.



| Método                                                                  | Descrição                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-synthetickeyboard-requeststatechange.md) | Solicita uma alteração de estado.<br/> |
| [**Redefinir**](msvm-synthetickeyboard-reset.md)                           | redefine o dispositivo.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ UserDevice**](cim-userdevice.md)
</dt> </dl>

 

 




