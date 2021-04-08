---
description: A reinicialização&\# 8194; O método de classe WMI desliga o sistema de computador e, em seguida, o reinicia.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Método reboot da classe Win32_OperatingSystem
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
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920508"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Método reboot da classe de sistema \_ operacional Win32

O método **reinicializar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) desliga o sistema de computador e, em seguida, o reinicia.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para códigos de erro, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Outro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

A capacidade de reiniciar programaticamente um computador permite que os administradores executem muitas tarefas de gerenciamento do computador remotamente.

Por exemplo, se você criar um script para instalar o software ou fazer uma alteração de configuração que exija a reinicialização de um computador, poderá incluir o comando de reinicialização no script e executar a operação inteira remotamente. O método **reboot** pode ser usado para reiniciar um computador. Como o método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , o método **reboot** exige que o usuário cujas credenciais de segurança estejam sendo usadas pelo script para ter o privilégio de desligamento.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir invoca o método reboot da classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .

> [!Note]  
> Você deve ter o privilégio de desligamento para invocar com êxito o método de desligamento.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



O código Perl a seguir invoca o método reboot da classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .

> [!Note]  
> Você deve ter o privilégio de desligamento para invocar com êxito o método de desligamento.

 


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



O VBScript a seguir invoca o método reboot da classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) em um sistema remoto. Preencha \_ \_ o nome do sistema remoto com o nome do sistema remoto para reinicializar.

> [!Note]  
> Você deve ter o privilégio RemoteShutdown para invocar com êxito o método de reinicialização

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Ele segue o Perl invoca o método reboot da classe [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) em um sistema remoto. Preencha \_ \_ o nome do sistema remoto com o nome do sistema remoto para reinicializar.

> [!Note]  
> Você deve ter o privilégio RemoteShutdown para invocar com êxito o método de reinicialização.

 


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
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Sistema \_ operacional Win32**](win32-operatingsystem.md)
</dt> <dt>

[**\_Método CIM OperatingSystem. Shutdown**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[Tarefas do WMI: gerenciamento de desktop](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

