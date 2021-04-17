---
description: A classe CommandLineEventConsumer inicia um processo arbitrário no sistema local quando um evento é entregue a ele.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: Classe CommandLineEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187935"
---
# <a name="commandlineeventconsumer-class"></a>Classe CommandLineEventConsumer

A classe **CommandLineEventConsumer** inicia um processo arbitrário no sistema local quando um evento é entregue a ele. Essa classe é um dos consumidores de eventos padrão que o WMI fornece. Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

> [!Note]  
> Ao usar a classe **CommandLineEventConsumer** , proteja o executável que você deseja iniciar. Se o executável não estiver em um local seguro, ou protegido com uma ACL (lista de controle de acesso) forte, um usuário não autorizado poderá substituir seu executável por um executável mal-intencionado. Para obter mais informações sobre ACLs, visite a seção segurança do SDK (Software Development Kit) do Microsoft Windows e veja [criando um descritor de segurança para um novo objeto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a>Membros

A classe **CommandLineEventConsumer** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CommandLineEventConsumer** tem essas propriedades.

<dl> <dt>

**CommandLineTemplate**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Modelo de cadeia de caracteres padrão que especifica o processo a ser iniciado. Essa propriedade pode ser **nula** e a propriedade **ExecutablePath** é usada como a linha de comando.

</dd> <dt>

**CreateNewConsole**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não usado. Se um valor for atribuído a essa propriedade, uma mensagem de rastreamento será gerada. Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).

</dd> <dt>

**CreateNewProcessGroup**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o novo processo será o processo raiz de um novo grupo de processos. O grupo de processos inclui todos os processos que são descendentes desse processo raiz. O identificador de processo do novo grupo de processos é o mesmo que esse identificador de processo. Os grupos de processos são usados pelo método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) para habilitar o envio de um sinal de CTRL + C ou Ctrl + Break para um grupo de processos de console.

</dd> <dt>

**CreateSeparateWowVdm**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o novo processo será executado em uma VDM (máquina virtual dos) privada. Isso só é válido ao iniciar um aplicativo em execução em um sistema operacional Windows de 16 bits. Se definido como **false**, todos os aplicativos executados em um sistema operacional Windows de 16 bits executarão como threads em um único VDM compartilhado. Para obter mais informações, consulte a seção comentários deste tópico.

</dd> <dt>

**CreateSharedWowVdm**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) executará o novo processo no VDM (computador virtual dos) compartilhado. Essa propriedade pode substituir a opção DefaultSeparateVDM na seção do Windows de Win.ini se definido como **true**. Para obter mais informações, consulte a seção comentários deste tópico.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

SID (identificador de segurança) que identifica exclusivamente o usuário que cria um filtro. O WMI armazena o SID do usuário que cria uma instância de [**\_ \_ EventConsumer**](--eventconsumer.md) ou o SID do administrador, dependendo do sistema operacional. Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) e [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Área de trabalho**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não usado. Se um valor for atribuído a essa propriedade, uma mensagem de rastreamento será gerada. Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Módulo a ser executado. A cadeia de caracteres pode especificar o caminho completo e o nome de arquivo do módulo a ser executado, ou pode especificar um nome parcial. Se um nome parcial for especificado, a unidade atual e o diretório atual serão assumidos.

A propriedade **ExecutablePath** pode ser **nula**. Nesse caso, o nome do módulo deve ser o primeiro token com delimitação de espaço em branco no valor da propriedade **CommandLineTemplate** . Se estiver usando um nome de arquivo longo que contenha um espaço, use cadeias de caracteres entre aspas para indicar onde o nome do arquivo termina e os argumentos começam a esclarecer o nome do arquivo.

> [!Note]  
> Como a propriedade **CommandLineTemplate** pode ser um modelo em que o módulo a ser executado é fornecido por uma variável, uma propriedade **ExecutablePath** **nula** permite o módulo especificado no parâmetro a ser executado e, em seguida, está fora do seu controle. Sempre defina a propriedade **ExecutablePath** no registro **CommandLineEventConsumer** para incluir o executável necessário, que evita a substituição por parâmetros de eventos. Se você precisar usar um modelo e uma variável para especificar o módulo a ser executado, tenha cuidado com quem recebe privilégio de gravação completa no namespace.

 

</dd> <dt>

**Fillattribute**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o texto inicial e as cores do plano de fundo se uma nova janela do console for criada em um aplicativo de console

</dd> <dt>

**FillAttributes**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Texto inicial e cores de plano de fundo, se uma nova janela de console for criada em um aplicativo de console. Essa propriedade é ignorada em um aplicativo de GUI. O valor pode ser qualquer combinação dos valores a seguir.

<dt>

1 (0x1)
</dt> <dd>

primeiro plano azul

</dd> <dt>

2 (0x2)
</dt> <dd>

primeiro plano verde

</dd> <dt>

4 (0x4)
</dt> <dd>

primeiro plano vermelho

</dd> <dt>

8 (0x8)
</dt> <dd>

intensidade do primeiro plano

</dd> <dt>

16 (0x10)
</dt> <dd>

plano de fundo azul

</dd> <dt>

32 (0x20)
</dt> <dd>

plano de fundo verde

</dd> <dt>

64 (0x40)
</dt> <dd>

plano de fundo vermelho

</dd> <dt>

128 (0x80)
</dt> <dd>

intensidade do plano de fundo

</dd> </dl>

Por exemplo, as seguintes combinações produzem texto vermelho em um plano de fundo branco:


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  ou  


```mof
0x74
```



</dd> <dt>

**ForceOffFeedback**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o cursor de comentários será forçado enquanto o processo estiver sendo iniciado. O cursor normal é exibido.

</dd> <dt>

**ForceOnFeedback**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o cursor estará no modo de comentários por dois segundos após o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ser chamado. Durante esses dois segundos, se o processo fizer a primeira chamada de GUI, o sistema fornecerá cinco mais segundos para o processo. Durante esses cinco segundos, se o processo mostrar uma janela, o sistema fornecerá outros cinco segundos para o processo concluir o desenho da janela.

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número, em segundos, que o serviço WMI aguarda antes de eliminar um processo 0 (zero) indica que um processo não deve ser eliminado. A eliminação de um processo impede que um processo seja executado indefinidamente.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do computador ao qual Instrumentação de Gerenciamento do Windows (WMI) envia eventos.

Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fila máxima para um consumidor específico, em bytes.

Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](key-qualifier.md)
</dt> </dl>

Nome exclusivo de um consumidor.

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Agendamento do nível de prioridade dos threads do processo. A lista a seguir lista os níveis de prioridade disponíveis.

<dt>

32 (0x20)
</dt> <dd>

Indica um processo normal sem necessidade de agendamento.

</dd> <dt>

64 (0x40)
</dt> <dd>

Indica um processo cujos threads são executados somente quando o sistema está ocioso e são admitidos pelos threads de qualquer processo em execução em uma classe de prioridade mais alta. Um exemplo é uma proteção de tela. A classe de prioridade ociosa é herdada por processos filho.

</dd> <dt>

128 (0x80)
</dt> <dd>

Indica um processo que executa tarefas de alta prioridade e de tempo crítico. Os threads de um processo de classe de alta prioridade sobrecapturam os threads de processos de classe de prioridade normal ou de prioridade ociosa. Um exemplo é o Lista de Tarefas, que deve responder rapidamente quando chamado pelo usuário, independentemente da carga no sistema. Use extrema atenção ao usar a classe de alta prioridade, porque um aplicativo vinculado à CPU com uma classe de alta prioridade pode usar quase todos os ciclos disponíveis.

</dd> <dt>

256 (0x100)
</dt> <dd>

Indica um processo que tem a maior prioridade possível. Os threads de um processo de classe de prioridade em tempo real apropriam os threads de todos os outros processos, incluindo processos do sistema operacional que executam tarefas importantes. Por exemplo, um processo em tempo real executado por mais de um breve intervalo pode fazer com que os caches de disco não sejam liberados ou fazer com que o mouse não responda.

</dd> </dl>

</dd> <dt>

**RunInteractively**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o processo será iniciado no WinStation interativo. Se **for false**, o processo será iniciado no serviço padrão WinStation. Essa propriedade substitui a propriedade **desktopname** . Essa propriedade só é usada localmente e somente se o usuário interativo for o mesmo usuário que configurou o consumidor.

A partir do Windows Vista, o processo que executa a instância **CommandLineEventConsumer** é iniciado na conta **LocalSystem** e está na sessão 0. Os serviços executados na sessão 0 não podem interagir com sessões de usuário.

</dd> <dt>

**ShowWindowCommand**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado de exibição da janela. Pode ser qualquer um dos valores que podem ser especificados no parâmetro *nCmdShow* para a função de [janela](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> <dt>

**UseDefaultErrorMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o modo de erro padrão será usado.

</dd> <dt>

**WindowTitle**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Título que aparece na barra de título do processo. Essa propriedade é ignorada para aplicativos de GUI.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Diretório de trabalho para este processo.

</dd> <dt>

**XCoordinate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

X-deslocamento, em pixels, da borda esquerda da tela até a borda esquerda da janela, se uma nova janela for criada.

</dd> <dt>

**XNumCharacters**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Largura do buffer de tela, em colunas de caracteres, se uma nova janela de console for criada. Essa propriedade é ignorada em um processo de GUI.

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Largura, em pixels, de uma nova janela, se uma nova janela for criada.

</dd> <dt>

**YCoordinate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Deslocamento Y, em pixels, da borda superior da tela até a borda superior da janela, se uma nova janela for criada.

</dd> <dt>

**YNumCharacters**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Altura do buffer de tela, em linhas de caracteres, se uma nova janela de console for criada. Essa propriedade é ignorada em um processo de GUI.

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Altura, em pixels, da nova janela, se uma nova janela for criada.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CommandLineEventConsumer** é derivada da classe abstrata [**\_ \_ EventConsumer**](--eventconsumer.md) .

A propriedade **CreateSeparateWowVdm** indica se o novo processo é executado em uma VDM (máquina virtual de dos) privada. A vantagem de executar separadamente é que uma falha só encerra o VDM. Programas executados em VDMs distintos continuam a funcionar normalmente, e os aplicativos baseados no Windows de 16 bits executados em VDMs separados têm filas de entrada separadas. Isso significa que, se um aplicativo parar de responder momentaneamente, os aplicativos em VDMs separados continuarão a receber a entrada. A desvantagem de executar separadamente é que ela leva muito mais memória para fazer isso. Você deve definir essa propriedade como **true** somente se o usuário solicitar que aplicativos baseados no Windows de 16 bits sejam executados em seu próprio VDM.

> [!Note]  
> O **CommandLineEventConsumer** usa o método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) internamente e passa as propriedades **ExecutablePath** e **CommandLineTemplate** como os parâmetros *lpApplicationName* e *lpCommandLine* . O exemplo de código de formato MOF (MOF) a seguir não usa **CommandLineEventConsumer** corretamente.

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



O método [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) passa *lpCommandLine* como `argv[0]` , `argv[1]` e assim por diante. Como `argv[0]` para aplicativos de 16 bits usados para serem reservados para o nome do arquivo executável, o código MOF anterior resulta no processo que está sendo criado, como se o comando a seguir fosse inserido no prompt de comando: **c: \\ Windows \\ System32 \\cscript.exe param1 param2**.

O comando anterior não é bem sucedido porque Cscript.exe não examina `argv[0]` e, portanto, não reconhece que ele não contém seu próprio nome, mas algo mais ("c: \\ \\ scripts \\ \\MyScript.js"). O exemplo a seguir identifica o uso recomendado de **CommandLineEventConsumer**.


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



O uso anterior de **CommandLineEventConsumer** resulta no processo criado como se o comando a seguir tivesse sido inserido no prompt de comando: **c: \\ Windows \\ system32 \\cscript.exe c: \\ scripts \\MyScript.js param1 param2**

Como "c: \\ \\ scripts \\ \\MyScript.js" é agora `argv[1]` , ele é visto por Cscript.exe e o comando é bem sucedido.

Para obter mais informações, consulte a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar o **CommandLineEventConsumer** para criar um consumidor, consulte [executando um programa da linha de comando com base em um evento](running-a-program-from-the-command-line-based-on-an-event.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Assinatura raiz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de consumidor padrão](standard-consumer-classes.md)
</dt> <dt>

[Monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Criando um consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

