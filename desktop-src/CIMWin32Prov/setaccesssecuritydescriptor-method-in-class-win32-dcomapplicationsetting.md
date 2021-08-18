---
description: Atualiza o descritor de segurança de acesso do aplicativo DCOM com um novo descritor de segurança definido por uma instância de uma classe \_ SecurityDescriptor win32.
ms.assetid: 71b708ba-5eb7-400e-bee2-37ca93966c3f
ms.tgt_platform: multiple
title: Método SetAccessSecurityDescriptor da Win32_DCOMApplicationSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab668b12d6f08e205c770f4c717eda6f996971897fedb48e70702fc2d80a3c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752686"
---
# <a name="setaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Método SetAccessSecurityDescriptor da classe \_ DCOMApplicationSetting do Win32

O **método SetAccessSecurityDescriptor** atualiza o descritor de segurança de acesso do aplicativo DCOM com um novo descritor de segurança definido por uma instância de uma classe [**\_ SecurityDescriptor win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Esse descritor de segurança controla quem tem permissão para acessar o aplicativo. A conta que executa o script ou aplicativo que chama esse método deve ter os privilégios **SeSecurityPrivilege** e **SeRestorePrivilege.** Para obter mais informações, consulte [Alterando a segurança de acesso em objetos securáveis.](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetAccessSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descritor* \[ Em\]
</dt> <dd>

O descritor de segurança a ser definido para o aplicativo DCOM.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro. Para obter mais informações, [consulte Códigos de retorno WMI](/windows/desktop/WmiSdk/wmi-return-codes) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Êxito**
</dt> <dd>

0

Conclusão bem-sucedida

</dd> <dt>

**2**
</dt> <dd>

O usuário não tem acesso às informações solicitadas

</dd> <dt>

**8**
</dt> <dd>

Falha desconhecida

</dd> <dt>

**9**
</dt> <dd>

O usuário não tem privilégios adequados para executar o método

</dd> <dt>

**21**
</dt> <dd>

Um parâmetro especificado na chamada de método é inválido

</dd> <dt>

**Outras**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**instância \_ securityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) e uma SACL [*(lista*](/windows/desktop/SecGloss/s-gly) de controle de acesso do sistema). Para obter mais informações, consulte [Listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **o SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado. Para obter mais informações, consulte [**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) [e Executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).

Você pode atualizar a DACL e a SACL na instância [**\_ do Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.

Os valores a seguir no [**SECURITY \_ DESCRIPTOR \_ CONTROL determinam**](/windows/desktop/SecAuthZ/security-descriptor-control) se a DACL, a SACL ou ambas são atualizadas.

-   **\_ES DACL \_ PRESENT**

    Indica que a DACL deve ser atualizada. Se isso não for definido, o WMI preservará o valor original da DACL.

-   **\_ES SACL \_ PRESENT**

    Indica que a SACL deve ser atualizada. Se isso não estiver definido, o WMI preservará o valor original da SACL. Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado. Para scripts, o nome do privilégio **é SeSecurityPrivilege.** Para obter mais informações, consulte [**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants).

Se as propriedades do usuário confiável grupo e proprietário não são **NULL,** elas são atualizadas. Caso contrário, o WMI preservará os valores originais. Para obter mais informações, consulte [Objetos do descritor de](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)segurança WMI .

Quando uma nova SACL é **NULL** em uma chamada para esse método, o SACL descritor de segurança no objeto passível de proteger de destino é deixado inalterado.

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

[**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos do descritor de segurança WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Alterando a segurança de acesso em objetos securáveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

