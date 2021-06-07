---
title: Método Create da classe Win32_Service (Serviços de Área de Trabalho Remota)
description: Método Create da classe Win32_Service (Serviços de Área de Trabalho Remota) – cria um novo serviço do sistema.
ms.assetid: 805754AA-B62A-4324-B289-503C42BEFA49
ms.tgt_platform: multiple
keywords:
- Criar Serviços de Área de Trabalho Remota do método
- Criar método Serviços de Área de Trabalho Remota, classe Win32_Service
- Classe Win32_Service Serviços de Área de Trabalho Remota, método Create
topic_type:
- apiref
api_name:
- Win32_Service.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b776d3e451d84c63be5bb61b98ed22081e1a29
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387115"
---
# <a name="create-method-of-the-win32_service-class-remote-desktop-services"></a>Método Create da classe Win32_Service (Serviços de Área de Trabalho Remota)

O método **Create** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cria um novo serviço do sistema.

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

Nome do serviço a ser instalado para o método **Create** . O comprimento máximo da cadeia de caracteres é de 256 caracteres. O banco de dados do Gerenciador de controle de serviço preserva o caso dos caracteres, mas comparações de nome de serviço sempre diferenciam maiúsculas de minúsculas. Barras invertidas (/) e barras invertidas duplas ( \\ \\ ) são caracteres de nome de serviço inválidos.

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

Tipo de serviços fornecidos para processos que os chamam.

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

Severidade do erro se o método **Create** falhar ao iniciar. O valor indica a ação tomada pelo programa de inicialização se ocorrer falha. Todos os erros são registrados pelo sistema.

<dt>

0
</dt> <dd>

O usuário não é notificado.

</dd> <dt>

1
</dt> <dd>

O usuário é notificado.

</dd> <dt>

2
</dt> <dd>

Sistema é reiniciado com a última configuração bem-sucedida conhecida.

</dd> <dt>

3
</dt> <dd>

O sistema tenta iniciar com uma configuração válida.

</dd> </dl> </dd> <dt>

*StartMode* \[ no\]
</dt> <dd>

Modo de início do serviço base do Windows.

<dt>

Inicialização
</dt> <dd>

Driver de dispositivo iniciado pelo carregador do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

Sistema
</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

Automática
</dt> <dd>

Serviço a ser iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.

</dd> <dt>

Manual
</dt> <dd>

Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](win32-terminalservice-startservice.md) .

</dd> <dt>

Desabilitado
</dt> <dd>

Serviço que não pode mais ser iniciado.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ no\]
</dt> <dd>

Se **for true**, o serviço poderá criar ou se comunicar com o Windows na área de trabalho.

</dd> <dt>

*Iniciar* \[ no\]
</dt> <dd>

Nome da conta sob a qual o serviço é executado. Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome do \\ usuário ou do formato UPN ( Username@DomainName ). O processo de serviço é registrado usando uma dessas duas formas quando é executado. Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado. Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem. Para um kernel ou drivers de nível de sistema, o *StartName* contém o nome do objeto de driver (ou seja, o sistema de \\ arquivos \\ rdr ou \\ \\ o driver XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo. Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço. Exemplo: DWDOM \\ admin.

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

Matriz de grupos de ordenação de carga que devem iniciar antes desse serviço. Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois valores **nulos** . Em Visual Basic ou script, você pode passar um vbArray. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador do grupo SC** (definido no arquivo Winsvc. h) para diferenciá-lo de um nome de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace. A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.

</dd> <dt>

*Imdependências* \[ no\]
</dt> <dd>

Matriz que contém nomes de serviços que devem ser iniciados antes do início desse serviço. Cada item na matriz é delimitado por **NULL** e a lista é encerrada por dois **valores NULL.** No Visual Basic ou script, você pode passar uma vbArray. Se o ponteiro for **NULL** ou se ele aponta para uma cadeia de caracteres vazia, o serviço não terá dependências. A dependência de um serviço significa que esse serviço só poderá ser executado se o serviço de que ele depende estiver em execução.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro. Para obter códigos de erro adicionais, [**consulte Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

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

O código de controle solicitado não pode ser enviado para o serviço porque o estado do serviço ( propriedade **State** da classe [**\_ Win32 BaseService)**](/windows/desktop/CIMWin32Prov/win32-baseservice) é igual a 0, 1 ou 2.

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

O caminho do diretório para o arquivo executável de serviço não foi encontrado.

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

Uma dependência de que esse serviço depende foi removida do sistema.

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

Esse serviço está sendo removido do sistema.

</dd> <dt>

**17**
</dt> <dd>

O serviço não tem nenhum thread de execução.

</dd> <dt>

**18**
</dt> <dd>

O serviço tem dependências circulares quando ele é iniciado.

</dd> <dt>

**19**
</dt> <dd>

Um serviço está em execução com o mesmo nome.

</dd> <dt>

**20**
</dt> <dd>

O nome do serviço tem caracteres inválidos.

</dd> <dt>

**21**
</dt> <dd>

Parâmetros inválidos foram passados para o serviço.

</dd> <dt>

**22**
</dt> <dd>

A conta na qual esse serviço é executado é inválida ou não tem as permissões para executar o serviço.

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

Os serviços geralmente são instalados de uma das duas maneiras: como parte da instalação do sistema operacional ou usando um programa de instalação fornecido pelo desenvolvedor de serviços. No entanto, alguns serviços, especialmente aqueles criados na empresa, podem não ter um programa de instalação. Nessas instâncias, você pode usar o **método Create** para instalar serviços programaticamente.

Apesar do nome, o método Create não cria um serviço de fato; ele simplesmente instala um serviço existente. Para usar esse comando, você precisa copiar o arquivo executável do serviço para um computador e, em seguida, usar **Criar** para instalar o serviço.

O **método Create** é semelhante ao método [**Change.**](win32-terminalservice-change.md) Em ambos os casos, as propriedades do serviço são passadas como parâmetros para o método . Assim como com os parâmetros usados com **o método Change,** a ordem na qual esses parâmetros são passados é muito importante.

O *parâmetro LoadOrderGroup* representa um grupo de serviços do sistema que definem dependências de execução. Os serviços devem ser iniciados na ordem especificada pelo Grupo de Ordem de Carregamento, pois os serviços dependem uns dos outros. Esses serviços dependentes exigem a presença dos serviços antecessores para funcionar corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Serviço \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Classes do sistema operacional](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[Tarefas WMI: Serviços](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

