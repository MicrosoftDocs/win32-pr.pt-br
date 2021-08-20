---
description: Representa o serviço de segurança. Ele é usado para definir as configurações de segurança do sistema virtual.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Classe Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32596a46abaa6d745223ab01f8da734e167909f01621deef85f0b21ddfc0b99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146891"
---
# <a name="msvm_securityservice-class"></a>\_Classe Msvm SecurityService

Representa o serviço de segurança. Ele é usado para definir as configurações de segurança do sistema virtual.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SecurityService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Msvm \_ SecurityService** tem esses métodos.



| Método                                                                                            | Descrição                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**GetKeyProtector**](msvm-securityservice-getkeyprotector.md)                                   | Método para recuperar o protetor de chave para um sistema virtual.<br/>   |
| [**ModifySecuritySettings**](msvm-securityservice-modifysecuritysettings.md)                     | Modifica as configurações de segurança atuais de uma máquina virtual.<br/> |
| [**RestoreLastKnownGoodKeyProtector**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | Método para restaurar de volta para o último protetor de chave válido conhecido.<br/> |
| [**SetKeyProtector**](msvm-securityservice-setkeyprotector.md)                                   | Método para definir o protetor de chave para um sistema virtual.<br/>        |
| [**Setsecuritypolicy**](msvm-securityservice-setsecuritypolicy.md)                               | Método para definir o protetor de chave para um sistema virtual.<br/>        |
| [**StartService**](msvm-securityservice-startservice.md)                                         | Inicia o serviço.<br/>                                          |
| [**StopService**](msvm-securityservice-stopservice.md)                                           | Interrompe o serviço.<br/>                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> </dl>

 

 




