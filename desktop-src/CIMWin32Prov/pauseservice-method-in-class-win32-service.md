---
description: Método PauseService da classe Win32_Service (Provedores WMI CIMWin32) – tenta colocar o serviço no estado pausado.
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: Método PauseService da classe Win32_Service (Provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d5546ef4c67a6c9fa23f723f45725b19999770e11771608e197d6b759ca61de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504536"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método PauseService da classe Win32_Service (Provedores WMI CIMWin32)

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tenta colocar o serviço no estado pausado.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 PauseService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**0**
</dt> <dd>

A solicitação foi aceita.

</dd> <dt>

**1**
</dt> <dd>

A solicitação não terá suporte.

</dd> <dt>

**2**
</dt> <dd>

O usuário não tinha o acesso necessário.

</dd> <dt>

**3**
</dt> <dd>

O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.

</dd> <dt>

**4**
</dt> <dd>

O código de controle pedido não é válido ou é inaceitável para o serviço.

</dd> <dt>

**5**
</dt> <dd>

O código de controle solicitado não pode ser enviado para o serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).**A** propriedade State) é igual a 0, 1 ou 2.

</dd> <dt>

**6**
</dt> <dd>

O serviço não foi iniciado.

</dd> <dt>

**7**
</dt> <dd>

O serviço não respondeu à solicitação de início em um tempo oportuno.

</dd> <dt>

**8**
</dt> <dd>

Falha desconhecida ao iniciar o serviço.

</dd> <dt>

**9**
</dt> <dd>

O caminho do diretório para o arquivo executável de serviço não foi encontrado.

</dd> <dt>

**10**
</dt> <dd>

O serviço já está em execução.

</dd> <dt>

**11**
</dt> <dd>

O banco de dados para adicionar um serviço novo está bloqueado.

</dd> <dt>

**12**
</dt> <dd>

Uma dependência de que esse serviço depende foi removida do sistema.

</dd> <dt>

**13**
</dt> <dd>

O serviço não localizou o serviço necessário em um serviço dependente.

</dd> <dt>

**14**
</dt> <dd>

O serviço foi desabilitado do sistema.

</dd> <dt>

**15**
</dt> <dd>

O serviço não tem a autenticação correta para ser executado no sistema.

</dd> <dt>

**16**
</dt> <dd>

Esse serviço está sendo removido do sistema.

</dd> <dt>

**17**
</dt> <dd>

O serviço não tem nenhum thread de execução.

</dd> <dt>

**18**
</dt> <dd>

O serviço tem dependências circulares quando ele é iniciado.

</dd> <dt>

**19**
</dt> <dd>

Um serviço está em execução com o mesmo nome.

</dd> <dt>

**20**
</dt> <dd>

O nome do serviço tem caracteres inválidos.

</dd> <dt>

**21**
</dt> <dd>

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>

**22**
</dt> <dd>

A conta na qual esse serviço é executado é inválida ou não tem as permissões para executar o serviço.

</dd> <dt>

**23**
</dt> <dd>

O serviço existe no banco de dados de serviços disponível no sistema.

</dd> <dt>

**24**
</dt> <dd>

O serviço está pausado atualmente no sistema.

</dd> </dl>

## <a name="remarks"></a>Comentários

Depois de determinar quais serviços podem ser interrompidos ou pausados, você pode usar os métodos [**StopService**](stopservice-method-in-class-win32-service.md) e [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) para parar e pausar serviços. A decisão de parar um serviço em vez de pausar ou vice-versa depende de vários fatores, incluindo o seguinte:

-   O serviço é capaz de ser pausado? Caso não seja, sua única opção é interromper o serviço.
-   Você precisa continuar tratando solicitações de cliente para alguém já conectado ao serviço? Em caso afirmativos, pausar um serviço normalmente permite que ele manipular clientes existentes ao negar acesso a novos clientes. Por outro lado, quando você para um serviço, todos os clientes são desconectados imediatamente.
-   Você precisa reconfigurar um serviço e fazer com que as alterações tenham efeito imediatamente? Embora as propriedades do serviço possam ser alteradas enquanto um serviço estiver em pausa, a maioria delas não tem efeito até que o serviço seja realmente interrompido e reiniciado.

O código de script necessário para interromper um serviço é quase idêntico ao código necessário para pausar o serviço.

## <a name="examples"></a>Exemplos

O [exemplo Pausar serviços em execução](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) em uma conta específica do VBScript pausa todos os serviços em execução na conta de serviço hipotética "Netsvc".

O exemplo de código VBScript a seguir demonstra como pausar um serviço específico de instâncias do [**Serviço Win32. \_**](win32-service.md)

> [!Note]  
> O serviço deve dar suporte à pausa e já estar em execução.

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



O exemplo de código Perl a seguir demonstra como pausar um serviço específico de instâncias do [**Serviço Win32. \_**](win32-service.md)

> [!Note]  
> O serviço deve dar suporte à pausa e já estar em execução.

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
    }
   } 
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Serviço \_ Win32**](win32-service.md)
</dt> <dt>

[Tarefas WMI: Serviços](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**StopService**](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

