---
description: Permite que o nome do grupo seja alterado.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Método Rename da classe Win32_Group
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
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755840"
---
# <a name="rename-method-of-the-win32_group-class"></a>Método Rename da classe de \_ grupo Win32

O método **Rename** da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) permite que o nome do grupo seja alterado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ do no\]
</dt> <dd>

Nome da conta de usuário do Windows no domínio especificado pela propriedade de **domínio** dessa classe.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método **Rename** pode retornar os códigos de erro listados na lista a seguir. Para valores inteiros diferentes daqueles listados, consulte códigos de [ \_ retorno do WMI](/windows/desktop/WmiSdk/wmi-return-codes).

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
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Grupo Win32**](win32-group.md)
</dt> <dt>

[**\_LogicalFileSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

