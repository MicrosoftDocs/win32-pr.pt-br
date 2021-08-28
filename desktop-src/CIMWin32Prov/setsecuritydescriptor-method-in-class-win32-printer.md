---
description: Grava uma versão atualizada do descritor de segurança que controla o acesso à impressora.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor da Win32_Printer classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8621c1977c4553f610299695c2c68a72f5a9d6f2ecfcbe6df46b8646c379c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958945"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a>Método SetSecurityDescriptor da classe Impressora \_ Win32

O **método SetSecurityDescriptor** grava uma versão atualizada do descritor de segurança que controla o acesso à impressora. O descritor de segurança é uma instância da [**classe \_ Win32 SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Para obter mais informações, consulte [Alterando a segurança de acesso em objetos securáveis.](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descritor* \[ Em\]
</dt> <dd>

O descritor de segurança associado à impressora.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**0**
</dt> <dd>

Conclusão bem-sucedida.

</dd> <dt>

**2**
</dt> <dd>

O usuário não tem acesso às informações solicitadas.

</dd> <dt>

**8**
</dt> <dd>

Falha desconhecida.

</dd> <dt>

**9**
</dt> <dd>

O usuário não tem privilégios adequados para executar o método.

</dd> <dt>

**21**
</dt> <dd>

Um parâmetro especificado na chamada de método não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**instância \_ securityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) e uma SACL [*(lista*](/windows/desktop/SecGloss/s-gly) de controle de acesso do sistema). Para obter mais informações, consulte [Listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **o SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado. Para obter mais informações, consulte [**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) [e Executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).

Você pode atualizar a DACL e a SACL na instância [**\_ SecurityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.

Os valores a seguir [**em SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determinam se a DACL, a SACL ou ambas são atualizadas.

-   **\_ES DACL \_ PRESENT**

    Indica que a DACL deve ser atualizada. Se isso não for definido, o WMI preservará o valor original da DACL.

-   **\_ES SACL \_ PRESENT**

    Indica que a SACL deve ser atualizada. Se isso não for definido, o WMI preservará o valor original da SACL. Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado. Para scripts, o nome do privilégio **é SeSecurityPrivilege.** Para obter mais informações, consulte [**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants).

Se as propriedades do usuário confiável grupo e proprietário não são **NULL,** elas são atualizadas. Caso contrário, o WMI preservará os valores originais. Para obter mais informações, consulte [Objetos do descritor de](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)segurança WMI .

Quando uma nova SACL é **NULL** em uma chamada para esse método, o SACL descritor de segurança no objeto passível de proteger de destino é deixado inalterado.

## <a name="examples"></a>Exemplos

O [exemplo do PowerShell Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) Substitua as permissões (ACL) de uma impressora para outra.

O exemplo de código do PowerShell a seguir descreve como definir o descritor de segurança para uma impressora.


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Impressora \_ Win32**](win32-printer.md)
</dt> <dt>

[**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos do descritor de segurança WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Alterando a segurança de acesso em objetos securáveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

