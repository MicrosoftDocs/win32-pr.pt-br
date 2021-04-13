---
description: Modifica um serviço do \_ SystemDriver Win32.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Método Change da classe Win32_SystemDriver (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457085"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Alterar o método da \_ classe systemdrive do Win32

O método **Change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifica um serviço [**de \_ systemdrive do Win32**](win32-systemdriver.md) . O parâmetro do grupo de [**\_ pedidos do Win32**](win32-loadordergroup.md) representa um agrupamento de serviços do sistema que definem dependências de execução. Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros. Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.

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

O nome para exibição do serviço. Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres. O nome é, por caso, preservado no Gerenciador de controle de serviço. As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.

Restrições: aceita o mesmo valor que o parâmetro de *nome* .

Exemplo: "atdisk"

</dd> <dt>

*Nome do caminho* \[ no\]
</dt> <dd>

O caminho totalmente qualificado para o arquivo executável que implementa o serviço.

Exemplo: *\\ systemroot \\ System32 \\ drivers \\afd.sys*

</dd> <dt>

*ServiceType* \[ no\]
</dt> <dd>

Tipo de serviços fornecidos aos processos que os chamam.

<dt>

1 (0x1)
</dt> <dd>

Driver de kernel

</dd> <dt>

2 (0x2)
</dt> <dd>

Driver do sistema de arquivos

</dd> <dt>

4 (0x4)
</dt> <dd>

Adaptador

</dd> <dt>

8 (0x8)
</dt> <dd>

Driver do reconhecedor

</dd> <dt>

16 (0x10)
</dt> <dd>

Próprio processo

</dd> <dt>

32 (0x20)
</dt> <dd>

Processo de compartilhamento

</dd> <dt>

256 (0x100)
</dt> <dd>

Processo interativo

</dd> </dl> </dd> <dt>

*ErrorControl* \[ no\]
</dt> <dd>

A severidade do erro se esse serviço não for iniciado durante a inicialização. O valor indica a ação tomada pelo programa de inicialização se ocorrer falha. Todos os erros são registrados pelo sistema.

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

O modo de início do serviço base do Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial**


</dt> <dd>

Driver de dispositivo iniciado pelo carregador do sistema operacional.

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicialização inicial**


</dt> <dd>

Driver de dispositivo que o carregador do sistema operacional inicia.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Início do sistema**


</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Início automático**


</dt> <dd>

Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Início da demanda**


</dt> <dd>

Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado**


</dt> <dd>

Serviço que não pode ser iniciado.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ no\]
</dt> <dd>

Um valor que, se **for verdadeiro**, o serviço pode criar ou se comunicar com as janelas na área de trabalho.

</dd> <dt>

*Iniciar* \[ no\]
</dt> <dd>

O nome da conta sob a qual o serviço é executado. Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome_do_domínio \\ username ou. \\ Usu. Quando ele é executado, o processo de serviço é registrado usando uma dessas duas formas. Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado. Se uma cadeia de caracteres vazia for especificada, o serviço será conectado como a conta LocalSystem. Para drivers de nível de kernel ou de sistema, *StartName* contém o nome do objeto de driver, por exemplo, \\ \\ o FileSystem rdr ou \\ \\ o driver XNS), que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo. Se **NULL** for especificado, o driver será executado com um nome de objeto padrão que o sistema de e/s cria com base no nome do serviço, por exemplo, DWDOM \\ admin.

Você também pode usar o formato UPN (nome principal do usuário) para especificar o **StartName**, por exemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ no\]
</dt> <dd>

A senha para o nome da conta especificada pelo parâmetro *StartName* . Especifique **NULL** se você não estiver alterando a senha. Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.

> [!Note]  
> Ao alterar um serviço de um sistema local para uma rede, ou de uma rede para um sistema local, *StartPassword* deve ser uma cadeia de caracteres vazia ("") e não **NULL**.

 

</dd> <dt>

*OrderGroup* \[ no\]
</dt> <dd>

O nome do grupo ao qual ele está associado. Os grupos de ordem de carregamento estão contidos no registro do sistema e determinam a sequência na qual os serviços são carregados no sistema operacional. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo. As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* . Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo. O registro do sistema tem uma lista de grupos de ordenação de carga localizados em:

**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ no\]
</dt> <dd>

A lista de grupos de ordenação de carga que devem iniciar antes do início desse serviço. A matriz é duplamente terminada por **nulo**. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo WinSvc. h) para diferenciá-los dos nomes de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace. A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.

</dd> <dt>

*Imdependências* \[ no\]
</dt> <dd>

A lista que contém os nomes dos serviços que devem iniciar antes do início desse serviço. A matriz é duplamente terminada por **nulo**. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. A dependência de um serviço significa que esse serviço pode ser executado somente se o serviço do qual ele depende estiver em execução.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de zero (0) se o serviço tiver sido modificado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Serviços dependentes em execução** (3)
</dt> <dt>

**Controle de serviço inválido** (4)
</dt> <dt>

O **serviço não pode aceitar o controle** (5)
</dt> <dt>

**Serviço não ativo** (6)
</dt> <dt>

**Tempo limite da solicitação de serviço** (7)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Caminho não encontrado** (9)
</dt> <dt>

**Serviço já em execução** (10)
</dt> <dt>

**Banco de dados de serviço bloqueado** (11)
</dt> <dt>

**Dependência de serviço excluída** (12)
</dt> <dt>

**Falha de dependência de serviço** (13)
</dt> <dt>

**Serviço desabilitado** (14)
</dt> <dt>

**Falha no logon do serviço** (15)
</dt> <dt>

**Serviço marcado para exclusão** (16)
</dt> <dt>

**Serviço sem thread** (17)
</dt> <dt>

**Dependência circular de status** (18)
</dt> <dt>

**Nome duplicado de status** (19)
</dt> <dt>

**Nome inválido do status** (20)
</dt> <dt>

**Parâmetro de status inválido** (21)
</dt> <dt>

**Conta de serviço inválida de status** (22)
</dt> <dt>

O **serviço de status existe** (23)
</dt> <dt>

**Serviço já pausado** (24)
</dt> <dt>

**Outro** (25 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

Para alterar um serviço de um serviço de rede para o sistema local, use os seguintes valores para os parâmetros *StartName* e *StartPassword* :


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Para alterar um serviço de um serviço do sistema local para um serviço de rede, use os seguintes valores para os parâmetros *StartName* e *StartPassword* :


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
| parâmetro<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Systemdrive do Win32 \_**](win32-systemdriver.md)
</dt> </dl>

 

