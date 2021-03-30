---
description: Tenta enviar um código de controle definido pelo usuário para um serviço.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Método UserControlService da classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826629"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a>Método UserControlService da classe Win32 \_ BaseService

O método da [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) tenta enviar um código de controle definido pelo usuário para um serviço.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ControlCode* \[ no\]
</dt> <dd>

Valor que especifica um comando de controle para um serviço. Por exemplo, um comando de controle é um comando "Pause" ou "Continue". O valor pode ser um código predefinido ou um valor e uma ação que o serviço define. Estes são os códigos de controle predefinidos:

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**\_continuação do controle de serviço \_**


</dt> <dd>

Notifica um serviço em pausa para retomar.

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**\_interrogação de controle de serviço \_**


</dt> <dd>

Notifica um serviço para relatar as informações de status atuais para o Gerenciador de controle de serviço.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**\_NETBINDADD de controle de serviço \_**


</dt> <dd>

Notifica um serviço de rede que há um novo componente para associação.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**\_NETBINDDISABLE de controle de serviço \_**


</dt> <dd>

Notifica um serviço de rede que uma de suas associações está desabilitada.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**\_NETBINDENABLE de controle de serviço \_**


</dt> <dd>

Notifica um serviço de rede de que uma associação desabilitada está habilitada.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**\_NETBINDREMOVE de controle de serviço \_**


</dt> <dd>

Notifica um serviço de rede que um componente para associação foi removido.

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**\_PARAMCHANGE de controle de serviço \_**


</dt> <dd>

Notifica um serviço de que seus parâmetros de inicialização são alterados.

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_pausa de controle de serviço \_**


</dt> <dd>

Notifica um serviço para pausar.

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_parada de controle de serviço \_**


</dt> <dd>

Notifica um serviço para parar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.

<dl> <dt>

**Êxito**
</dt> <dd>

0

A solicitação é aceita.

</dd> <dt>

**Sem suporte**
</dt> <dd>

1

A solicitação não terá suporte.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

O usuário não tem os direitos de acesso necessários.

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

O serviço não iniciou.

</dd> <dt>

**Tempo limite da solicitação de serviço**
</dt> <dd>

7

O serviço não responde à solicitação de início rapidamente.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

8

Processo interativo.

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

Uma dependência da qual esse serviço depende é removida do sistema.

</dd> <dt>

**Falha na dependência de serviço**
</dt> <dd>

13

O serviço não encontra o serviço necessário de um serviço dependente.

</dd> <dt>

**Serviço desabilitado**
</dt> <dd>

14

O serviço está desabilitado no sistema.

</dd> <dt>

**Falha no logon do serviço**
</dt> <dd>

15

O serviço não tem a autenticação correta para ser executado no sistema.

</dd> <dt>

**Serviço marcado para exclusão**
</dt> <dd>

16

O serviço está sendo removido do sistema.

</dd> <dt>

**Serviço sem thread**
</dt> <dd>

17

Não há nenhum thread de execução para o serviço.

</dd> <dt>

**Dependência circular de status**
</dt> <dd>

18

Há dependências circulares quando o serviço é iniciado.

</dd> <dt>

**Nome duplicado de status**
</dt> <dd>

19

Há um serviço em execução com o mesmo nome.

</dd> <dt>

**Nome inválido do status**
</dt> <dd>

20

Há caracteres inválidos no nome do serviço.

</dd> <dt>

**Parâmetro de status inválido**
</dt> <dd>

21

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>

**Conta de serviço inválida de status**
</dt> <dd>

22

A conta em que esse serviço é executado não é válida ou não tem as permissões para executar o serviço.

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

[**\_BaseService Win32**](win32-baseservice.md)
</dt> </dl>

 

