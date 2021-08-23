---
description: Cria um serviço novo.
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Criar método da classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 827a82bf76fe78b86f97efa3aa01e0ae1106cd81430952b5d5b2849b5b3dd492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547426"
---
# <a name="create-method-of-the-win32_baseservice-class"></a>Criar método da classe BaseService Win32 \_

O **método** [criar classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo serviço. O *parâmetro LoadOrderGroup* representa um grupo de serviços do sistema que definem dependências de execução. Os serviços devem ser iniciados na ordem especificada pelo Grupo de Ordem de Carregamento, pois os serviços dependem uns dos outros. Esses serviços dependentes exigem a presença dos serviços antecessores para funcionar corretamente.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ Em\]
</dt> <dd>

Nome do serviço a ser instalado no **método** Create. O comprimento máximo da cadeia de caracteres é de 256 caracteres. O banco de dados do gerenciador de controle de serviço preserva o caso dos caracteres, mas as comparações de nome de serviço sempre não fazem maiúsculas de minúsculas. Barras (/) e barras in back duplas ( ) são \\ caracteres de nome de serviço inválidos.

</dd> <dt>

*DisplayName* \[ Em\]
</dt> <dd>

Nome de exibição do serviço. Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres. O nome é preservado em caso no gerenciador de controle de serviço. *As comparações* de DisplayName sempre não fazem maiúsculas de minúsculas.

Restrições: aceita o mesmo valor que o *parâmetro* Name.

Exemplo: "Atdisk".

</dd> <dt>

*PathName* \[ Em\]
</dt> <dd>

Caminho totalmente qualificado para o arquivo executável que implementa o serviço.

Exemplo: \\ "Drivers SystemRoot \\ System32 \\ \\afd.sys".

</dd> <dt>

*ServiceType* \[ Em\]
</dt> <dd>

Tipo de serviços fornecidos para processos que os chamam. O valor é um bitmap.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Driver de kernel** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Driver do sistema de** arquivos (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptador** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Driver do Reconhecedor** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Processo próprio** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processo de compartilhamento** (32)


</dt> <dd></dd> <dt>

256
</dt> <dd>

Processo interativo

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

*ErrorControl* \[ Em\]
</dt> <dd>

Severidade do erro se o **método Create** não for iniciar. O valor indica a ação tomada pelo programa de inicialização se ocorrer uma falha. Todos os erros são registrados pelo sistema.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** (0)


</dt> <dd>

O usuário não é notificado.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)


</dt> <dd>

O usuário é notificado.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (2)


</dt> <dd>

Sistema é reiniciado com a última configuração bem-sucedida conhecida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)


</dt> <dd>

O sistema tenta começar com uma boa configuração.

</dd> </dl> </dd> <dt>

*StartMode* \[ Em\]
</dt> <dd>

Modo de início do serviço Windows base.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")


</dt> <dd>

Driver de dispositivo iniciado pelo carregador do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Início do Sistema** ("Sistema")


</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início Automático** ("Automático")


</dt> <dd>

Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")


</dt> <dd>

Serviço a ser iniciado pelo gerenciador de controle de serviço quando um processo chama o [**método StartService.**](startservice-method-in-class-win32-service.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** ("Desabilitado")


</dt> <dd>

Serviço que não pode mais ser iniciado.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ Em\]
</dt> <dd>

Se **for true,** o serviço poderá criar ou se comunicar com janelas na área de trabalho.

</dd> <dt>

*StartName* \[ Em\]
</dt> <dd>

Nome da conta sob a qual o serviço é executado. Dependendo do tipo de serviço, o nome da conta pode estar na forma de "Nome de usuário \\ domainname". O processo de serviço é registrado usando um desses dois formulários quando ele é executado. Se a conta pertencer ao domínio integrado, ". \\ Nome de usuário" pode ser especificado. Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem. Para um kernel ou drivers no nível do sistema, *StartName* contém o nome do objeto do driver (ou seja, FileSystem Rdr ou Driver Xns) que o sistema de entrada e saída \\ \\ \\ (E/S) usa para carregar o driver de \\ dispositivo. Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de E/S com base no nome do serviço. Exemplo: Administrador \\ DWDOM.

</dd> <dt>

*StartPassword* \[ Em\]
</dt> <dd>

Senha para o nome da conta especificado pelo *parâmetro StartName.* **Especifique NULL** se você não estiver alterando a senha. Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.

</dd> <dt>

*LoadOrderGroup* \[ Em\]
</dt> <dd>

Nome do grupo associado ao novo serviço. Os grupos de ordem de carregamento estão contidos no Registro e determinam a sequência na qual os serviços são carregados no sistema operacional. Se o ponteiro for **NULL ou** se ele aponta para uma cadeia de caracteres vazia, o serviço não pertence a um grupo. As dependências entre grupos devem ser listadas no *parâmetro LoadOrderGroupDependencies.* Os serviços na lista de grupos de pedidos de carga são iniciados primeiro, seguidos por serviços em grupos que não estão na lista de grupos de pedidos de carga, seguidos por serviços que não pertencem a um grupo. O Registro tem uma lista de grupos de ordenação de carga localizados em:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ Em\]
</dt> <dd>

Matriz de grupos de ordenação de carga que devem iniciar antes desse serviço. Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois **valores NULL.** No Visual Basic ou script, você pode passar uma vbArray. Se o ponteiro for **NULL ou** se ele aponta para uma cadeia de caracteres vazia, o serviço não terá dependências. Os nomes de grupo devem ser prefixados pelo caractere SC GROUP IDENTIFIER (definido no arquivo \_ Winsvc.h) para diferenciá-lo de um nome de serviço, porque serviços e grupos de serviços compartilham o mesmo \_ namespace. A dependência em um grupo significa que esse serviço poderá ser executado se pelo menos um membro do grupo estiver em execução após uma tentativa de iniciar todos os membros do grupo.

</dd> <dt>

*ServiceDependencies* \[ Em\]
</dt> <dd>

Matriz que contém nomes de serviços que devem ser iniciados antes do início desse serviço. Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois **valores NULL.** No Visual Basic ou script, você pode passar uma vbArray. Se o ponteiro for **NULL** ou se ele aponta para uma cadeia de caracteres vazia, o serviço não terá dependências. A dependência de um serviço significa que esse serviço só poderá ser executado se o serviço de que ele depende estiver em execução.

</dd> </dl>

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

 

