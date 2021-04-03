---
description: Obtém o descritor de segurança que controla quem tem permissão para configurar um aplicativo DCOM.
ms.assetid: 2858a7a0-1e5b-47aa-9967-0f578c3c22c1
ms.tgt_platform: multiple
title: Método GetConfigurationSecurityDescriptor da classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 320af05b352641c812c51353c2e7bda0da046bb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646307"
---
# <a name="getconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Método GetConfigurationSecurityDescriptor da classe Win32 \_ DCOMApplicationSetting

O método WMI **GetConfigurationSecurityDescriptor** Obtém o descritor de segurança que controla quem tem permissão para configurar um aplicativo DCOM. O descritor de segurança é uma instância da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . A conta que executa o script ou o aplicativo que chama esse método deve ter os privilégios **SeSecurityPrivilege** e **SeRestorePrivilege** . Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetConfigurationSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descritor* \[ fora\]
</dt> <dd>

O descritor de segurança a ser definido para o aplicativo DCOM.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro. Para obter mais informações, consulte [códigos de retorno do WMI](/windows/desktop/WmiSdk/wmi-return-codes) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

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

**Abril**
</dt> <dd>

Um parâmetro especificado na chamada do método é inválido

</dd> <dt>

**Outras**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema. Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado. Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).

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

[**\_DCOMApplicationSetting Win32**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos do descritor de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Alterando a segurança de acesso em objetos protegíveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

