---
description: O método excluir classe WMI exclui um serviço existente.
ms.assetid: 040005a0-9584-4458-bd1e-a2d50f53a637
ms.tgt_platform: multiple
title: Método Delete da classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8dab8d11ab6d30cf6d3e8dd2de41913e72bd0a67990275dff61f0794b33ce7b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547416"
---
# <a name="delete-method-of-the-win32_baseservice-class"></a>Método Delete da classe Win32 \_ BaseService

O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) exclui um serviço existente.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.

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

O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço (Propriedade de [**estado**](win32-baseservice.md) [**\_ BaseService do Win32**](win32-baseservice.md)) é igual a 0, 1 ou 2.

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

A conta na qual esse serviço deve ser executado é inválida ou não tem as permissões para executar o serviço.

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

 

