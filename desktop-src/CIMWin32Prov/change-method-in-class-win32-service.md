---
description: Modifica um serviço Win32 \_ .
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: Método Change da classe Win32_Service (Mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501018"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a>Método Change da classe Win32_Service (Mbnapi. h)

O método **Change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifica um [**\_ serviço Win32**](win32-service.md).

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
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

Restrições: aceita o mesmo valor que a propriedade **Name** .

Exemplo, "atdisk".

</dd> <dt>

*Nome do caminho* \[ no\]
</dt> <dd>

O caminho totalmente qualificado para o arquivo executável que implementa o serviço, por exemplo, " \\ systemroot \\ System32 \\ drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ no\]
</dt> <dd>

O tipo de serviços fornecidos aos processos que os chamam.

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

Severidade do erro se esse serviço não for iniciado durante a inicialização. O valor indica a ação tomada pelo programa de inicialização se ocorrer falha. Todos os erros são registrados pelo sistema.

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

Modo de início do serviço base do Windows. Para obter mais informações, consulte a seção Comentários.

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

Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-service.md) .

</dd> <dt>

Desabilitado
</dt> <dd>

Serviço que não pode mais ser iniciado.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ no\]
</dt> <dd>

Se **for true**, o serviço poderá criar ou se comunicar com uma janela na área de trabalho.

</dd> <dt>

*Iniciar* \[ no\]
</dt> <dd>

Nome da conta sob a qual o serviço é executado. Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome_do_domínio \\ username ou. \\ Usu. O processo de serviço será registrado usando uma dessas duas formas quando for executado. Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado. Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem. Para drivers de nível de kernel ou de sistema, *StartName* contém o nome do objeto de driver (ou seja, \\ FileSystem \\ rdr ou o \\ Driver \\ XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo. Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço, por exemplo, "DWDOM \\ admin".

Você também pode usar o formato UPN (nome principal do usuário) para especificar o **StartName**, por exemplo, *Username@DomainName* .

</dd> <dt>

*StartPassword* \[ no\]
</dt> <dd>

Senha para o nome da conta especificada pelo parâmetro *StartName* . Especifique **NULL** se você não estiver alterando a senha. Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.

> [!Note]  
> Ao alterar um serviço de um sistema local para uma rede, ou de uma rede para um sistema local, *StartPassword* deve ser uma cadeia de caracteres vazia ("") e não **NULL**.

 

</dd> <dt>

*OrderGroup* \[ no\]
</dt> <dd>

Nome do grupo ao qual ele está associado. Os grupos de ordem de carregamento estão contidos no registro do sistema e determinam a sequência na qual os serviços são carregados no sistema operacional. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo. Para obter mais informações, consulte a seção Comentários.

As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* . Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo. O registro do sistema tem uma lista de grupos de ordenação de carga localizados em:

**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ no\]
</dt> <dd>

Lista de grupos de ordenação de carga que devem iniciar antes do início desse serviço. A matriz é duplamente terminada por **nulo**. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador de grupo SC** (definido no arquivo Winsvc. h) para diferenciá-los dos nomes de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace. A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.

</dd> <dt>

*Imdependências* \[ no\]
</dt> <dd>

Lista que contém os nomes dos serviços que devem ser iniciados antes do início desse serviço. A matriz é duplamente terminada por **nulo**. Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências. A dependência em um serviço indica que esse serviço pode ser executado somente se o serviço do qual ele depende estiver em execução.

</dd> </dl>

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

## <a name="remarks"></a>Comentários

Quando um computador é iniciado, todos os serviços de inicialização automática também são iniciados. Na ocasião, um desses serviços pode falhar ao iniciar junto com o computador. Quando um serviço falha durante a inicialização do sistema, o computador executa uma ação com base no valor do código de controle de erro do serviço.

a maioria dos serviços é instalada usando o código de controle de erro normal. Algumas das exceções, que são instaladas usando o código de erro ignorar, incluem:

-   Serviço de Replicação de Arquivos
-   Cartão inteligente
-   Logon Secundário
-   WMI

Para os serviços instalados usando o código de erro de ignorar, nenhuma notificação é dada ao usuário de que o serviço falhou. Se preferir a notificação na tela informando que um serviço não pôde ser iniciado, você poderá usar o WMI para alterar o código de controle de erro. Códigos de controle de erro se aplicam somente à inicialização do computador; os códigos de controle de erro não serão usados se você parar e, em seguida, tentar reiniciar um serviço depois que o computador estiver em execução.

Na ocasião, talvez seja necessário alterar a conta sob a qual um determinado serviço é executado. Por exemplo, você pode executar um serviço em uma conta administrativa. Como isso pode criar uma vulnerabilidade de segurança, você pode alternar o serviço para uma conta com menos privilégios. Como alternativa, você pode ter serviços em execução em uma conta que está prestes a ser excluída, ou talvez queira garantir que, em todos os servidores, determinados serviços sejam executados em determinadas contas. Você pode usar o método **Change** da classe [**de \_ serviço do Win32**](win32-service.md) para configurar os serviços para serem executados em uma conta de usuário especificada. Ao selecionar uma conta, tenha em mente o seguinte:

-   A conta que está sendo usada como uma conta de serviço deve ter o direito de fazer logon como um serviço. Esse direito pode ser concedido usando Política de Grupo.
-   A conta que está sendo usada como uma conta de serviço não deve ser membro de um grupo local, de domínio ou de administradores de empresa.
-   Cada instância de um serviço deve ser executada em uma conta de usuário exclusiva. Isso fornece segurança adicional e habilita a auditoria de instâncias de serviço individuais.
-   Se o serviço for interativo, o serviço deverá ser executado na conta LocalSystem.

    O LocalSystem é necessário porque apenas uma estação de janela (WinSta0) pode ser visível e interativa por vez. Se um serviço for executado em uma conta diferente de LocalSystem, ele será executado na estação de janela padrão Service-0x03E7 $ \\ , que é uma janela invisível. Os serviços em execução nesta estação de janela não podem receber entrada ou exibir a saída.

Quando você atribui uma conta a um serviço, o SCM requer a senha correta para essa conta antes de fazer a atribuição. Se você fornecer uma senha incorreta, o SCM rejeitará a conta. Se você configurar uma conta de serviço usando a conta LocalSystem, LocalService ou NetworkService, não será necessário fornecer uma senha de conta, pois essas contas não têm senhas.

O SCM armazena a senha da conta no banco de dados de serviços. No entanto, depois que a senha é atribuída, o SCM não garante que a senha armazenada no banco de dados de serviços e a senha atribuída à conta de usuário no Active Directory continuem a corresponder. Consequentemente, uma situação semelhante à seguinte pode ocorrer:

-   Você configura um serviço para ser executado em uma conta de usuário específica.
-   O serviço é iniciado sob essa conta usando a senha da conta atual.
-   Você altera a senha da conta de usuário.
-   O serviço continua a ser executado. No entanto, se o serviço for interrompido, você não poderá reiniciá-lo porque o SCM continua a usar a senha antiga e inválida. Alterar a senha em Active Directory não altera a senha armazenada no banco de dados de serviços.

Se você executar serviços em contas de usuário regulares, precisará atualizar essas senhas de serviço sempre que a senha da conta de usuário for alterada. Isso pode ser particularmente demorado se você não tiver certeza de quais serviços estão sendo executados nessa conta ou quais computadores têm serviços em execução nessa conta. Felizmente, você pode usar o WMI para verificar as contas de serviço em todos os seus computadores e, se necessário, alterar a senha da conta de serviço.

O parâmetro do [**\_ Sqlorder OrderGroup do Win32**](win32-loadordergroup.md) representa um grupo de serviços do sistema que definem dependências de execução. Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros. Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.

Para alterar um serviço de um serviço de rede para um sistema local, os parâmetros *StartName* e *StartPassword* devem ter os seguintes valores:


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Para alterar um serviço de um serviço do sistema local para uma rede, os parâmetros *StartName* e *StartPassword* devem ter os seguintes valores:


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a>Exemplos

O VBScript a seguir altera a conta de serviço para que os serviços sejam executados em uma conta de usuário especificada para LocalSystem.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



O VBScript a seguir altera a senha da conta de serviço para todos os scripts em execução em netsvc


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
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

[**\_Serviço Win32**](win32-service.md)
</dt> <dt>

[Tarefas do WMI: serviços](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

