---
description: Modifica um objeto de serviço derivado do Win32 \_ BaseService.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Método Change da classe Win32_BaseService (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 306f771df0e44cb11ec61631b2d6b51f11ccefac9a719776d3a483d5cc861133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085826"
---
# <a name="change-method-of-the-win32_baseservice-class"></a>Método Change da classe Win32 \_ BaseService

O método **Change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifica um objeto de serviço derivado de [**Win32 \_ BaseService**](win32-baseservice.md). O parâmetro do [**\_ Sqlorder OrderGroup do Win32**](win32-loadordergroup.md) representa um grupo de serviços do sistema que definem dependências de execução. Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros. Esses serviços dependentes exigem que os serviços antecedentes funcionem corretamente.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Change(
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

*DisplayName* \[ no\]
</dt> <dd>

O nome de exibição de um serviço. Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres. O nome é o caso preservado no Gerenciador de controle de serviço. As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.

Restrições: aceita o mesmo valor que o parâmetro de *nome* .

Exemplo: "atdisk".

</dd> <dt>

*Nome do caminho* \[ no\]
</dt> <dd>

O caminho totalmente qualificado para o arquivo executável que implementa um serviço.

Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ no\]
</dt> <dd>

Tipo de serviços fornecidos para processos que os chamam.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Driver de kernel** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Driver do sistema de arquivos** (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adaptador** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Driver do reconhecedor** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Próprio processo** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Processo de compartilhamento** (32)


</dt> <dd></dd> <dt>



 (256)


</dt> <dd>

Processo interativo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ no\]
</dt> <dd>

Severidade de um erro se esse serviço não for iniciado durante a inicialização. O valor indica a ação que o programa de inicialização executará se ocorrer uma falha. O sistema registra todos os erros.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** (0)


</dt> <dd>

O usuário não é notificado.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)


</dt> <dd>

Normal. O usuário é notificado.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severo** (2)


</dt> <dd>

O sistema é reiniciado com a última configuração válida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (3)


</dt> <dd>

O sistema tenta reiniciar com uma configuração adequada.

</dd> </dl> </dd> <dt>

*StartMode* \[ no\]
</dt> <dd>

modo de início do serviço base de Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial** ("inicialização")


</dt> <dd>

Driver de dispositivo que o carregador do sistema operacional inicia.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Início do sistema** ("sistema")


</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático** ("automático")


</dt> <dd>

Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda** ("manual")


</dt> <dd>

Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-baseservice.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")


</dt> <dd>

Serviço que não pode ser iniciado.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ no\]
</dt> <dd>

Se **for true**, o serviço poderá criar ou se comunicar com uma janela na área de trabalho.

</dd> <dt>

*Iniciar* \[ no\]
</dt> <dd>

Nome da conta sob a qual o serviço é executado, o que depende do tipo de serviço. O nome da conta pode estar na forma de DomainName \\ username ou. \\ Usu. Quando é executado, o processo de serviço é registrado usando uma das duas formas anteriores. Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado. Se uma cadeia de caracteres vazia for especificada, o serviço será conectado como a conta LocalSystem. Para drivers de nível de kernel ou de sistema, *StartName* contém o nome do objeto de driver, por exemplo, \\ \\ o FileSystem rdr ou \\ \\ o driver XNS, que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo. Se **NULL** for especificado, o driver será executado com um nome de objeto padrão que o sistema de e/s cria com base no nome do serviço, por exemplo, DWDOM \\ admin.

Você também pode usar o formato UPN (nome principal do usuário) para especificar o **StartName**, por exemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ no\]
</dt> <dd>

Senha para o nome da conta que o parâmetro *StartName* especifica. Especifique **NULL** quando você não alterar a senha. Especifique uma cadeia de caracteres vazia se o serviço não tiver uma senha.

> [!Note]  
> Quando você altera um serviço do sistema local para a rede ou da rede para o sistema local, *StartPassword* deve ser uma cadeia de caracteres vazia ("") e não **NULL**.

 

</dd> <dt>

*OrderGroup* \[ no\]
</dt> <dd>

Nome do grupo ao qual ele está associado. Os grupos de ordem de carregamento estão contidos no registro do sistema e determinam a sequência em que os serviços são carregados em um sistema operacional. Se o ponteiro for **nulo** ou apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo. As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* . Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo. O registro do sistema tem uma lista de grupos de ordenação de carga localizados em **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.

</dd> <dt>

*LoadOrderGroupDependencies* \[ no\]
</dt> <dd>

Lista de grupos de ordenação de carga que devem iniciar antes do início desse serviço. A matriz é duplamente terminada por **nulo**. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo Winsvc. h) para diferenciá-los dos nomes de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace. A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.

</dd> <dt>

*Imdependências* \[ no\]
</dt> <dd>

Lista que contém os nomes dos serviços que devem ser iniciados antes do início desse serviço. A matriz é duplamente terminada por **nulo**. Se o ponteiro for **nulo** ou apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. A dependência de um serviço significa que esse serviço pode ser executado somente se o serviço do qual ele depende estiver em execução.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

O usuário não tem os privilégios de acesso necessários.

</dd> <dt>

**Serviços dependentes em execução**
</dt> <dd>

3

O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.

</dd> <dt>

**Controle de serviço inválido**
</dt> <dd>

4

O código de controle solicitado não é válido ou é inaceitável para o serviço.

</dd> <dt>

**O serviço não pode aceitar o controle**
</dt> <dd>

5

O código de controle solicitado não pode ser enviado ao serviço porque a propriedade [**State**](win32-baseservice.md) no [**objeto \_ BaseService do Win32**](win32-baseservice.md) é igual a 0, 1 ou 2.

</dd> <dt>

**Serviço não ativo**
</dt> <dd>

6

O serviço não foi iniciado.

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

Uma dependência para a qual esse serviço depende é removida do sistema.

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

A conta para a qual este serviço será executado não é válida ou não tem as permissões para executar o serviço.

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

## <a name="remarks"></a>Comentários

Para alterar um serviço de uma rede para um sistema local, use os seguintes valores para os parâmetros *StartName* e *StartPassword* :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Para alterar um serviço de um sistema local para uma rede, use os seguintes valores para os parâmetros *StartName* e *StartPassword* :


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_BaseService Win32**](win32-baseservice.md)
</dt> </dl>

 

