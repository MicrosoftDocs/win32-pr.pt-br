---
description: Permite que o nome do grupo seja alterado.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Renomear o método da Win32_Group classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cff8f587426b45133716e308ea40785602fea2d5b5d30a99645bfd0c6cc5c4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003016"
---
# <a name="rename-method-of-the-win32_group-class"></a>Renomear o método da classe De grupo \_ Win32

O **método de classe** [WMI Renomear](/windows/desktop/WmiSdk/retrieving-a-class) permite que o nome do grupo seja alterado.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ Em\]
</dt> <dd>

Nome da Windows de usuário no domínio especificado pela **propriedade Domain** dessa classe.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **método Renomear** pode retornar os códigos de erro listados na lista a seguir. Para valores inteiros diferentes daqueles listados, consulte [Códigos de \_ retorno WMI](/windows/desktop/WmiSdk/wmi-return-codes).

<dl> <dt>

**Êxito**
</dt> <dd>

0

Sucesso.

</dd> <dt>

**Instância não encontrada**
</dt> <dd>

1

</dd> <dt>

**Instância necessária**
</dt> <dd>

2

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

3

</dd> <dt>

**Grupo não encontrado**
</dt> <dd>

4

</dd> <dt>

**Domínio não encontrado**
</dt> <dd>

5

</dd> <dt>

**A operação é permitida somente no controlador de domínio primário do domínio**
</dt> <dd>

6

</dd> <dt>

**A operação não é permitida em grupos especiais especificados; usuário, administrador, local ou convidado.**
</dt> <dd>

7

</dd> <dt>

**Outro erro de API**
</dt> <dd>

8

</dd> <dt>

**Erro interno**
</dt> <dd>

9

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Grupo \_ Win32**](win32-group.md)
</dt> <dt>

[**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

