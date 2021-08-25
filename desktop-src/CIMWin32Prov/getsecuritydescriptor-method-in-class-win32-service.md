---
description: Método GetSecurityDescriptor da classe Win32_Service (Provedores WMI CIMWin32) – retorna o descritor de segurança que controla o acesso ao serviço.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor da classe Win32_Service (Provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3d48974ecfae4cd932ed58718dded4b54b382317d269fea30ac450d8b05ef75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878776"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método GetSecurityDescriptor da classe Win32_Service (Provedores WMI CIMWin32)

O **método GetSecurityDescriptor** retorna o descritor de segurança que controla o acesso ao serviço. O descritor é retornado como uma instância de [**\_ SecurityDescriptor do Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Descritor* \[ out\]
</dt> <dd>

O descritor de segurança associado ao serviço.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Êxito**
</dt> <dd>

0

A solicitação foi aceita.

</dd> <dt>


</dt> <dd>

1

A solicitação não terá suporte.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

O usuário não tinha o acesso necessário.

</dd> <dt>


</dt> <dd>

3

O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.

</dd> <dt>


</dt> <dd>

4

O código de controle pedido não é válido ou é inaceitável para o serviço.

</dd> <dt>


</dt> <dd>

5

O código de controle solicitado não pode ser enviado para o serviço porque o estado do serviço ([**Win32 \_ BaseService**](win32-baseservice.md).**A** propriedade State) é igual a 0, 1 ou 2.

</dd> <dt>


</dt> <dd>

6

O serviço não foi iniciado.

</dd> <dt>


</dt> <dd>

7

O serviço não respondeu à solicitação de início em um tempo oportuno.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

8

Falha desconhecida ao iniciar o serviço.

</dd> <dt>

**Privilégio ausente**
</dt> <dd>

9

O caminho do diretório para o arquivo executável de serviço não foi encontrado.

</dd> <dt>


</dt> <dd>

10

O serviço já está em execução.

</dd> <dt>


</dt> <dd>

11

O banco de dados para adicionar um serviço novo está bloqueado.

</dd> <dt>


</dt> <dd>

12

Uma dependência de que esse serviço depende foi removida do sistema.

</dd> <dt>


</dt> <dd>

13

O serviço não localizou o serviço necessário em um serviço dependente.

</dd> <dt>


</dt> <dd>

14

O serviço foi desabilitado do sistema.

</dd> <dt>


</dt> <dd>

15

O serviço não tem a autenticação correta para ser executado no sistema.

</dd> <dt>


</dt> <dd>

16

Esse serviço está sendo removido do sistema.

</dd> <dt>


</dt> <dd>

17

O serviço não tem nenhum thread de execução.

</dd> <dt>


</dt> <dd>

18

O serviço tem dependências circulares quando ele é iniciado.

</dd> <dt>


</dt> <dd>

19

Um serviço está em execução com o mesmo nome.

</dd> <dt>


</dt> <dd>

20

O nome do serviço tem caracteres inválidos.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

21

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>


</dt> <dd>

22

A conta na qual esse serviço é executado é inválida ou não tem as permissões para executar o serviço.

</dd> <dt>


</dt> <dd>

23

O serviço existe no banco de dados de serviços disponível no sistema.

</dd> <dt>


</dt> <dd>

24

O serviço está pausado atualmente no sistema.

</dd> <dt>

**Outras**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**instância \_ securityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário) e uma SACL [*(lista*](/windows/desktop/SecGloss/s-gly) de controle de acesso do sistema). Para obter mais informações, consulte [Listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).

Se **o SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado. Para obter mais informações, consulte [**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) [e Executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Exemplos

Ao recuperar um descritor de segurança no VBScript, certifique-se de "Segurança" e execute como Administrador, conforme mostrado no snippet de código a seguir. Caso contrário, seu código poderá lançar um erro de permissões.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



Da mesma forma, VB.NET, certifique-se de definir "EnablePrivileges = True" e executar o Aplicativo como Administrador.


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
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

[**Serviço \_ Win32**](win32-service.md)
</dt> <dt>

[**Constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos do descritor de segurança WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Alterando a segurança de acesso em objetos securáveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

