---
description: A reinicialização&\# 8194; O método de classe WMI desliga o sistema de computador e, em seguida, reinicia-o.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Método de reinicialização da Win32_OperatingSystem classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 700d497650e8950c72467bbad8e11cf450b2302f0b68ef762e8a11e3c6aaceee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752726"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Método de reinicialização da classe OperatingSystem Win32 \_

O **método** [de classe WMI de](/windows/desktop/WmiSdk/retrieving-a-class) reinicialização desliga o sistema de computador e, em seguida, reinicia-o.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para códigos de erro, [**consulte Constantes de**](/windows/desktop/WmiSdk/wmi-error-constants) erro WMI ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Outros** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

A capacidade de reiniciar programaticamente um computador permite que os administradores executem muitas tarefas de gerenciamento de computador remotamente.

Por exemplo, se você criar um script para instalar o software ou fazer uma alteração de configuração que exija a reinicialização de um computador, poderá incluir o comando de reinicialização no script e executar toda a operação remotamente. O **método Reboot** pode ser usado para reiniciar um computador. Assim como [**o método Win32Shutdown,**](win32shutdown-method-in-class-win32-operatingsystem.md) o método **Reboot** requer que o usuário cujas credenciais de segurança estão sendo usadas pelo script para ter o privilégio Desligamento.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir invoca o método Reboot da [**classe \_ OperatingSystem Win32.**](win32-operatingsystem.md)

> [!Note]  
> Você deve ter o privilégio Desligamento para invocar com êxito o método Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



O código Perl a seguir invoca o método Reboot da [**classe \_ OperatingSystem Win32.**](win32-operatingsystem.md)

> [!Note]  
> Você deve ter o privilégio Desligamento para invocar com êxito o método Shutdown.

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



O VBScript a seguir invoca o método Reboot da [**classe \_ OperatingSystem Win32**](win32-operatingsystem.md) em um sistema remoto. Preencha REMOTE \_ SYSTEM NAME com o nome do sistema remoto a ser \_ reinicializado.

> [!Note]  
> Você deve ter o privilégio RemoteShutdown para invocar com êxito o método Reboot

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



ele seguindo Perl invoca o método Reboot da [**classe Win32 \_ OperatingSystem**](win32-operatingsystem.md) em um sistema remoto. Preencha REMOTE \_ SYSTEM NAME com o nome do sistema remoto a ser \_ reinicializado.

> [!Note]  
> Você deve ter o privilégio RemoteShutdown para invocar com êxito o método Reboot.

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



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

[**Sistema operacional \_ Win32**](win32-operatingsystem.md)
</dt> <dt>

[**Método CIM \_ OperatingSystem.Shutdown**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[Tarefas WMI: Gerenciamento de Área de Trabalho](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

