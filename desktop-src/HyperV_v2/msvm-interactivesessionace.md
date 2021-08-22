---
description: Representa uma ACE (entrada de controle de acesso) que determina o acesso à sessão interativa de uma máquina virtual.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Classe Msvm_InteractiveSessionACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed7dd4c4a3742f43a3de8e919ae2200e76cacc03ba1f7da066f48bac018f0a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148379"
---
# <a name="msvm_interactivesessionace-class"></a>\_Classe Msvm InteractiveSessionACE

Representa uma ACE ( *entrada de controle de acesso* ) que determina o acesso à sessão interativa de uma máquina virtual.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ InteractiveSessionACE** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ InteractiveSessionACE** tem essas propriedades.

<dl> <dt>

**AccessType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a ACE concede ou nega o acesso ao Trustee.

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

**Acesso permitido** (0)


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

**Acesso negado** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Confiança**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica a entidade de segurança que o ACE concede ou nega acesso ao. os formatos válidos para essa propriedade incluem o Windows formato de nome de usuário compatível com SAM e o formato de cadeia de caracteres de SID de Windows.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetInteractiveSessionACL**](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




