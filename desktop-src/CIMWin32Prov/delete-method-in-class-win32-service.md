---
description: Método Delete da classe Win32_Service (provedores WMI CIMWin32)-a exclusão&\# 8194; O método de classe WMI exclui um serviço existente.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Método Delete da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4031184e23e99fc54237ed0b0b4196fe6c075c5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089574"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método Delete da classe Win32_Service (provedores WMI CIMWin32)

O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui um serviço existente.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Delete();
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

**aprimora**
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

À medida que sua organização for alterada, você poderá optar por remover determinados serviços de determinados computadores. Os serviços internos e de terceiros podem ser removidos usando o WMI, enquanto os serviços do sistema operacional podem ser removidos usando Sysocmgr.exe.

Ao se preparar para remover os serviços, tenha em mente as seguintes informações:

-   Os serviços devem ser interrompidos antes de serem removidos. Se o serviço estiver em execução quando você emitir o comando delete, o serviço será marcado para exclusão, mas continuará sendo executado até que seja interrompido e todos os identificadores abertos sejam fechados.

    Se o serviço nunca for interrompido, esse serviço nunca será excluído.

-   A remoção de um serviço não remove o arquivo executável do serviço.

    A remoção de um serviço usando o WMI exclui as entradas de registro relacionadas em HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services. Como resultado, o serviço não é mais instalado e não está disponível por meio do snap-in serviços. No entanto, o WMI não exclui o arquivo executável, o que significa que você pode facilmente reinstalar o serviço. Para excluir o arquivo executável, você deve recuperar o nome do caminho e, em seguida, excluir o arquivo.

-   Remover um serviço base do Windows 2000 (por exemplo, DHCP) usando o WMI exclui as entradas do registro para esse serviço, mas não remove o atalho do menu Ferramentas administrativas ou remove o serviço do assistente de componentes do Windows. Isso pode confundir qualquer pessoa que tentar determinar como o computador foi configurado.

    Por exemplo, se você remover o serviço DHCP usando um script WMI, o serviço DHCP não estará mais listado no snap-in serviços. No entanto, um atalho não funcional para o console do DHCP permanece no menu Ferramentas administrativas e, se você iniciar o assistente de componentes do Windows, ele indicará que o serviço DHCP está instalado.

    Por isso, você sempre deve usar Sysocmgr.exe para remover programaticamente os serviços do Windows 2000.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir descreve como excluir um serviço.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



O exemplo de código Perl a seguir descreve como excluir um serviço.


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Serviço Win32**](win32-service.md)
</dt> <dt>

[Tarefas do WMI: serviços](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

