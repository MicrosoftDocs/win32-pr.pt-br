---
description: Coloca o serviço, representado pelo objeto de \_ serviço do Win32, no estado parado.
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: Método StopService da classe Win32_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c8c055c260f4983622010ced5de652cf673391b7ae02a75b40fd28427a78827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751876"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a>Método StopService da classe Win32_Service (Sdoias. h)

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca o serviço, representado pelo objeto de [**\_ serviço do Win32**](win32-service.md) , no estado parado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

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

O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).**** A propriedade State) é igual a 0, 1 ou 2.

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

O caminho do diretório para o arquivo executável do serviço não foi encontrado.

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

Uma dependência da qual esse serviço depende foi removida do sistema.

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

Este serviço está sendo removido do sistema.

</dd> <dt>

**17**
</dt> <dd>

O serviço não tem nenhum thread de execução.

</dd> <dt>

**anos**
</dt> <dd>

O serviço tem dependências circulares quando é iniciado.

</dd> <dt>

**19**
</dt> <dd>

Um serviço está sendo executado com o mesmo nome.

</dd> <dt>

**20**
</dt> <dd>

O nome do serviço tem caracteres inválidos.

</dd> <dt>

**Abril**
</dt> <dd>

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>

**22**
</dt> <dd>

A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.

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

Depois de determinar quais serviços podem ser interrompidos ou pausados, você pode usar os métodos **StopService** e [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) para parar e pausar serviços. A decisão de interromper um serviço em vez de pausá-lo, ou vice-versa, depende de vários fatores, incluindo o seguinte:

-   O serviço é capaz de ser pausado? Caso contrário, sua única opção é parar o serviço.
-   Você precisa continuar tratando as solicitações do cliente para qualquer pessoa já conectada ao serviço? Nesse caso, pausar um serviço geralmente permite que ele manipule clientes existentes enquanto nega acesso a novos clientes. Por outro lado, quando você interrompe um serviço, todos os clientes são imediatamente desconectados.
-   Você precisa reconfigurar um serviço e fazer com que as alterações entrem em vigor imediatamente? Embora as propriedades do serviço possam ser alteradas enquanto um serviço é pausado, a maioria delas não tem efeito até que o serviço seja realmente interrompido e reiniciado.

O código de script necessário para interromper um serviço é quase idêntico ao código necessário para pausar o serviço.

Se você tentar interromper um serviço que tem serviços dependentes em execução, o método **StopService** falhará com um valor de retorno de 3. Os serviços dependentes devem ser interrompidos primeiro.

Se você parar um serviço, verifique imediatamente o [**\_ serviço Win32**](win32-service.md).**** A propriedade State, pois o valor ainda pode mostrar o serviço como em execução.

## <a name="examples"></a>Exemplos

[O set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) O exemplo do PowerShell define o estado do serviço para máquinas remotas.

O exemplo de [parar um serviço e seus dependentes](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) do VBScript interrompe um serviço e todos os serviços dependentes.

O exemplo de código VBScript a seguir demonstra como desligar um serviço.


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



O exemplo de código Perl a seguir demonstra como desligar um serviço.


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



O exemplo de código VBScript a seguir mostra que você não pode interromper o serviço NetDDE até que os serviços dependentes tenham sido interrompidos. Para executar o script, verifique se o serviço NetDDE e seus serviços dependentes estão em execução usando o snap-in do MMC Services. msc ou o comando **net start** .

A classe [**Win32 \_ DependentService**](win32-dependentservice.md) permite que você localize dependências de serviço por meio [de um associador de](/windows/desktop/WmiSdk/associators-of-statement) consulta.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Serviço Win32**](win32-service.md)
</dt> <dt>

[Tarefas do WMI: serviços](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**PauseService**](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 

