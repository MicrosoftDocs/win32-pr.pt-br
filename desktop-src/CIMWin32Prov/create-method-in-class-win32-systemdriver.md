---
description: Cria um novo serviço gerenciado pelo driver do sistema.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Método Create da classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a85b18a04672f63c4f1fd8fe4fa386ffb4e3094e817b53a20af9887a84748a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080150"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Criar método da \_ classe systemdrive do Win32

O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo serviço gerenciado pelo driver do sistema. O parâmetro do grupo de *\_ pedidos do Win32* representa um agrupamento de serviços do sistema que definem dependências de execução. Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros. Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

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

*Nome* \[ do no\]
</dt> <dd>

Nome do serviço a ser instalado para o método **Create** . O comprimento máximo da cadeia de caracteres é de 256 caracteres. O banco de dados do Gerenciador de controle de serviço preserva o caso dos caracteres, mas comparações de nome de serviço sempre diferenciam maiúsculas de minúsculas. Barras invertidas (/) e barras invertidas duplas ( \\ ) são caracteres de nome de serviço inválidos.

</dd> <dt>

*DisplayName* \[ no\]
</dt> <dd>

Nome de exibição do serviço. Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres. O nome é, por caso, preservado no Gerenciador de controle de serviço. As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.

Restrições: aceita o mesmo valor que o parâmetro de *nome* .

Exemplo: "atdisk".

</dd> <dt>

*Nome do caminho* \[ no\]
</dt> <dd>

Caminho totalmente qualificado para o arquivo executável que implementa o serviço.

Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys".

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

Severidade do erro se o método **Create** falhar ao iniciar. Esse valor indica a ação realizada pelo programa de inicialização se ocorrer falha. Todos os erros são registrados pelo sistema.

<dt>

0
</dt> <dd>

Ignorar

O usuário não é notificado.

</dd> <dt>

1
</dt> <dd>

"Normal"

O usuário é notificado.

</dd> <dt>

2
</dt> <dd>

Muito

Sistema é reiniciado com a última configuração bem-sucedida conhecida.

</dd> <dt>

3
</dt> <dd>

Drasticamente

O sistema tenta iniciar com uma configuração válida.

</dd> </dl> </dd> <dt>

*StartMode* \[ no\]
</dt> <dd>

modo de início do serviço base de Windows.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização**


</dt> <dd>

Driver de dispositivo iniciado pelo carregador do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**


</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**


</dt> <dd>

Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**


</dt> <dd>

Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado**


</dt> <dd>

Serviço que não pode mais ser iniciado.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ no\]
</dt> <dd>

Se **for true**, o serviço poderá criar ou se comunicar com as janelas na área de trabalho.

</dd> <dt>

*Iniciar* \[ no\]
</dt> <dd>

Nome da conta sob a qual o serviço é executado. Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome do \\ usuário ou do formato UPN ( Username@DomainName ). O processo de serviço é registrado usando uma dessas duas formas quando é executado. Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado. Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem. Para um kernel ou drivers de nível de sistema, o *StartName* contém o nome do objeto de driver (ou seja, o sistema de \\ arquivos \\ rdr ou \\ \\ o driver XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo. Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.

Exemplo: administrador do DWDOM \\

</dd> <dt>

*StartPassword* \[ no\]
</dt> <dd>

Senha para o nome da conta especificada pelo parâmetro *StartName* . Especifique **NULL** se você não estiver alterando a senha. Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.

</dd> <dt>

*OrderGroup* \[ no\]
</dt> <dd>

Nome do grupo associado ao novo serviço. Os grupos de ordem de carregamento estão contidos no registro e determinam a sequência na qual os serviços são carregados no sistema operacional. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo. As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* . Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo. O registro tem uma lista de grupos de ordenação de carga localizados em:

**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ no\]
</dt> <dd>

Matriz de grupos de ordenação de carga que devem iniciar antes desse serviço. Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** . em Visual Basic ou script, você pode passar um vbArray. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo Winsvc. h) para diferenciá-lo de um nome de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace. A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.

</dd> <dt>

*Imdependências* \[ no\]
</dt> <dd>

Uma matriz que contém os nomes de serviços que devem ser iniciados antes do início desse serviço. Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** . em Visual Basic ou script, você pode passar um vbArray. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. A dependência de um serviço significa que esse serviço só poderá ser executado se o serviço do qual ele depende estiver em execução.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) se o serviço foi criado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.

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

[**Systemdrive do Win32 \_**](win32-systemdriver.md)
</dt> </dl>

 

