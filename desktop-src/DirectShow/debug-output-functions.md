---
description: Funções de saída de depuração
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Funções de saída de depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252e1020ca99bd5b4f2f46d7f2169fa6835dea83a25d599dba142f370bb794f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537736"
---
# <a name="debug-output-functions"></a>Funções de saída de depuração

as [Classes Base DirectShow](directshow-base-classes.md) fornecem várias macros para exibir informações de depuração.



| Função                                               | Descrição                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DbgCheckModuleLevel**](dbgcheckmodulelevel.md)     | Verifica se o log está habilitado para os tipos e o nível de mensagem fornecidos.                             |
| [**DbgDumpObjectRegister**](dbgdumpobjectregister.md) | Exibe informações sobre objetos ativos.                                                           |
| [**DbgInitialise**](dbginitialise.md)                 | Inicializa a biblioteca de depuração.                                                                       |
| [**DbgLog**](dbglog.md)                               | Envia uma cadeia de caracteres para o local de saída de depuração, se o registro em log estiver habilitado para o tipo e o nível especificados. |
| [**DbgOutString**](dbgoutstring.md)                   | Envia uma cadeia de caracteres para o local de saída de depuração.                                                         |
| [**DbgSetModuleLevel**](dbgsetmodulelevel.md)         | Define o nível de log para um ou mais tipos de mensagem.                                                |
| [**DbgTerminate**](dbgterminate.md)                   | Limpa a biblioteca de depuração.                                                                         |
| [**TipoDeExibição**](displaytype.md)                     | Envia informações sobre um tipo de mídia para o local de saída de depuração.                                   |
| [**DumpGraph**](dumpgraph.md)                         | Envia informações sobre um grafo de filtro para o local de saída de depuração.                                 |
| [**GuidNames**](guidnames.md)                         | Matriz global que contém cadeias de caracteres que representam os GUIDs definidos em UUIDs. h.                        |
| [**NOMES**](name.md)                                   | Gera uma cadeia de caracteres somente depuração.                                                                       |
| [**ANOTAÇÕES**](note.md)                                   | Envia uma cadeia de caracteres para o local de saída de depuração.                                                         |
| [**-**](remind.md)                               | Gera um lembrete no tempo de compilação.                                                                |



 

**Chaves do registro**

a função debug output no DirectShow usar um conjunto de chaves do registro. O local dessas chaves do registro depende da versão do Windows.

*antes do Windows Vista*, as chaves de depuração estão localizadas no seguinte caminho:

**HKEY \_ \_** Depuração de \\ **software** \\  de computador local

no Windows Vista ou posterior, eles estão localizados no seguinte caminho:

**HKEY \_ \_computador LOCAL** \\ **SOFTWARE** \\ **Microsoft** \\ **DirectShow** \\ **Debug**

para filtros de terceiros, o local depende de qual versão do [DirectShow Classes Base](directshow-base-classes.md) foi usada para criar o filtro. a versão incluída no SDK do Windows para Windows Vista usa o caminho mais recente. As versões anteriores usaram o caminho mais antigo.

Nos comentários a seguir, o rótulo *<DebugRoot>* é usado para indicar esses dois caminhos. substitua o caminho correto, dependendo da versão do Windows ou da versão das classes base.

**Log de depuração**

DirectShow define vários tipos de mensagem, mostrados na tabela a seguir.



| Valor                   | Descrição                                             |
|-------------------------|---------------------------------------------------------|
| erro de LOG \_              | Notificação de erro.                                     |
| bloqueio de LOG \_            | Bloqueio e desbloqueio de seções críticas.             |
| memória de LOG \_             | Alocação de memória e criação e destruição de objetos. |
| tempo de LOG \_             | Medições de tempo e desempenho.                    |
| rastreamento de LOG \_              | Rastreamento de chamada geral.                                   |
| PERSONALIZADO1 por meio de CUSTOM5 | Disponível para mensagens de depuração personalizadas                     |



 

cada uma das DirectShow funções de log de depuração especifica um tipo de mensagem e um nível de log. A mensagem de depuração é exibida somente quando o nível de depuração atual para esse tipo de mensagem é igual ou maior que o nível especificado na função de log. Caso contrário, a mensagem será ignorada.

Por exemplo, o código a seguir gera a cadeia de caracteres "esta é uma mensagem de depuração" se o nível de rastreamento de LOG \_ for 3 ou superior:

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

Cada módulo pode definir seu próprio nível de depuração para cada tipo de mensagem. (Um *módulo* é uma DLL ou um executável que pode ser carregado usando a função **LoadLibrary** .) Os níveis de depuração de um módulo aparecem no registro na seguinte chave:

**\_máquina local \_ HKEY**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**

em que *<Message Type>* é o tipo de mensagem menos o "log \_ " inicial; por exemplo, **bloqueio** para mensagens de bloqueio de log \_ . Quando um módulo é carregado, a biblioteca de depuração localiza os níveis de log do módulo no registro. Se as chaves do registro não existirem, a biblioteca de depuração as criará.

Um módulo também pode definir seus próprios níveis em tempo de execução, usando a função [**DbgSetModuleLevel**](dbgsetmodulelevel.md) . Para enviar uma mensagem para a saída de depuração, chame a macro [**DbgLog**](dbglog.md) . O exemplo a seguir cria uma mensagem de nível 3 do tipo rastreamento de LOG \_ :

Você também pode especificar níveis de log globais, com a seguinte chave do registro:


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



A biblioteca de depuração usa qualquer nível que seja maior, o nível global ou o nível de módulo.

**Local de saída de depuração**

O local de saída de depuração é determinado por outra chave do registro:

**HKEY \_ \_Máquina local** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile**

Se o valor dessa chave for `Console` , a saída vai para a janela do console. Se o valor for `Deb` , `Debug` , `Debugger` ou uma cadeia de caracteres vazia, a saída vai para a janela do depurador. Caso contrário, a saída será gravada em um arquivo especificado pela chave do registro.

antes que um executável use a biblioteca de depuração DirectShow, ele deve chamar a função [**DbgInitialise**](dbginitialise.md) . Depois disso, ele deve chamar a função [**DbgTerminate**](dbgterminate.md) . As DLLs não precisam chamar essas funções, porque o ponto de entrada de DLL (definido na biblioteca de classes base) as chama automaticamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Utilitários de depuração](debugging-utilities.md)
</dt> </dl>

 

 



