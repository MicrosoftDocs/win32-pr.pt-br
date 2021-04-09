---
description: Modifica o modo de início de um \_ serviço Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Método ChangeStartMode da classe Win32_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010177"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método ChangeStartMode da classe Win32_Service (provedores WMI CIMWin32)

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica o modo de início de [**um \_ serviço Win32**](win32-service.md).

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartMode* \[ no\]
</dt> <dd>

Modo de início do serviço base do Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")


</dt> <dd>

Driver de dispositivo iniciado pelo carregador do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")


</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático** ("automático")


</dt> <dd>

Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")


</dt> <dd>

Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-service.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")


</dt> <dd>

Serviço que não pode mais ser iniciado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Êxito**
</dt> <dd>

0

A solicitação foi aceita.

</dd> <dt>

**Sem suporte**
</dt> <dd>

1

A solicitação não terá suporte.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

O usuário não tinha o acesso necessário.

</dd> <dt>

**Serviços dependentes em execução**
</dt> <dd>

3

O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.

</dd> <dt>

**Controle de serviço inválido**
</dt> <dd>

4

O código de controle pedido não é válido ou é inaceitável para o serviço.

</dd> <dt>

**O serviço não pode aceitar o controle**
</dt> <dd>

5

O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).**** A propriedade State) é igual a 0, 1 ou 2.

</dd> <dt>

**Serviço não ativo**
</dt> <dd>

6

O serviço não foi iniciado.

</dd> <dt>

**Tempo limite da solicitação de serviço**
</dt> <dd>

7

O serviço não respondeu à solicitação de início em um tempo oportuno.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

8

Falha desconhecida ao iniciar o serviço.

</dd> <dt>

**Caminho não encontrado**
</dt> <dd>

9

O caminho do diretório para o arquivo executável do serviço não foi encontrado.

</dd> <dt>

**Serviço já em execução**
</dt> <dd>

10

O serviço já está em execução.

</dd> <dt>

**Banco de dados de serviço bloqueado**
</dt> <dd>

11

O banco de dados para adicionar um serviço novo está bloqueado.

</dd> <dt>

**Dependência de serviço excluída**
</dt> <dd>

12

Uma dependência da qual esse serviço depende foi removida do sistema.

</dd> <dt>

**Falha na dependência de serviço**
</dt> <dd>

13

O serviço não localizou o serviço necessário em um serviço dependente.

</dd> <dt>

**Serviço desabilitado**
</dt> <dd>

14

O serviço foi desabilitado do sistema.

</dd> <dt>

**Falha no logon do serviço**
</dt> <dd>

15

O serviço não tem a autenticação correta para ser executado no sistema.

</dd> <dt>

**Serviço marcado para exclusão**
</dt> <dd>

16

Este serviço está sendo removido do sistema.

</dd> <dt>

**Serviço sem thread**
</dt> <dd>

17

O serviço não tem nenhum thread de execução.

</dd> <dt>

**Dependência circular de status**
</dt> <dd>

18

O serviço tem dependências circulares quando é iniciado.

</dd> <dt>

**Nome duplicado de status**
</dt> <dd>

19

Um serviço está sendo executado com o mesmo nome.

</dd> <dt>

**Nome inválido do status**
</dt> <dd>

20

O nome do serviço tem caracteres inválidos.

</dd> <dt>

**Parâmetro de status inválido**
</dt> <dd>

21

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>

**Conta de serviço inválida de status**
</dt> <dd>

22

A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.

</dd> <dt>

**O serviço de status existe**
</dt> <dd>

23

O serviço existe no banco de dados de serviços disponível no sistema.

</dd> <dt>

**O serviço já está em pausa**
</dt> <dd>

24

O serviço está pausado atualmente no sistema.

</dd> <dt>

**Outras**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="examples"></a>Exemplos

A seguinte [alteração de StartMode de um exemplo do](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell de serviço, extraído da galeria do TechNet, altera o modo de início de um serviço.


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
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

[**\_Serviço Win32**](win32-service.md)
</dt> <dt>

[Tarefas do WMI: serviços](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

