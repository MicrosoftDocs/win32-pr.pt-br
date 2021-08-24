---
description: A lista&\# 8194; O método de classe WMI descarrega programas e DLLs até que seja seguro desligar o computador.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Método shutdown da classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 068551ee013634bde9a42584764c36f255bf322bedb97e6ebb3a5075c113e742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800836"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Método de desligamento da classe OperatingSystem Win32 \_

O **método de** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de desligamento descarrega programas e DLLs até que seja seguro desligar o computador.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Shutdown();
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

Ocasionalmente, os computadores precisam ser removidos da rede, talvez para manutenção agendada, porque o computador não está funcionando corretamente ou para concluir um processo de configuração. Por exemplo, se um servidor DHCP estiver entregando endereços IP errados, talvez você queira desligar o computador até que um técnico de serviço possa ser enviado para corrigir o problema. Se você suspeitar que ocorreu uma violação de segurança, talvez seja necessário desligar determinados servidores para garantir que eles não possam ser acessados até que o problema de segurança seja resolvido. Algumas operações de configuração (como alterar um nome de computador) exigem que você reinicie o computador antes que a alteração entre em vigor.

Esse método desliga imediatamente o computador, se possível. O sistema interrompe todos os processos em execução, libera todos os buffers de arquivo para o disco e, em seguida, alimenta o sistema. O processo de chamada deve ter o **ES de NOME \_ \_ DE DESLIGAMENTO,** conforme descrito no exemplo a seguir.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Para obter mais informações sobre como definir um privilégio, consulte [Executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations) e [executando operações privilegiadas usando o VBScript.](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript) Para obter opções de desligamento adicionais, como um logoff ou um desligamento forçado, consulte o [**método Win32Shutdown.**](win32shutdown-method-in-class-win32-operatingsystem.md)

## <a name="examples"></a>Exemplos

O código VBScript a seguir desliga o computador local.

> [!Note]  
> Você deve ter o privilégio Desligamento para invocar com êxito o método Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



O código Perl a seguir desliga o computador local.

> [!Note]  
> Você deve ter o privilégio Desligamento para invocar com êxito o método Shutdown.

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



O código VBScript a seguir desliga o computador remoto especificado. Preencha REMOTE *\_ SYSTEM \_ NAME* com o nome do sistema remoto a ser desligado.

> [!Note]  
> Você deve ter o privilégio RemoteShutdown para invocar com êxito o **método Shutdown.**

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
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

[Tarefas WMI: Gerenciamento de Área de Trabalho](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Executando operações privilegiadas usando o VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

