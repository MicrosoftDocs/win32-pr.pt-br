---
description: Quando um usuário clica com o botão direito do mouse em um objeto do Shell, como um arquivo, o Shell exibe um menu de atalho (contexto).
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: Verbos e associações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a144051b04ef2d9a2c9877b53e1680d4274afc92d3fc87fbcb531b02a0f94946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860783"
---
# <a name="verbs-and-file-associations"></a>Verbos e associações de arquivo

Quando um usuário clica com o botão direito do mouse em um objeto do Shell, como um arquivo, o Shell exibe um menu de atalho (contexto). Esse menu contém uma lista de comandos que o usuário pode selecionar para executar várias ações no item. Esses comandos também são conhecidos como itens de menu de atalho ou verbos. Os menus de atalho podem ser personalizados.

Este tópico é organizado da seguinte maneira:

-   [Introdução aos menus de atalho para objetos do sistema de arquivos](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Adicionar comandos a um menu de atalho](#add-commands-to-a-shortcut-menu)
-   [Verbos do menu de atalho](#shortcut-menu-verbs)
-   [transmitir itens de sistema sem arquivos e resultados de OpenSearch.](#stream-non-file-system-items-and-opensearch-results)
-   [Registrar um aplicativo para lidar com tipos de arquivo arbitrários](#register-an-application-to-handle-arbitrary-file-types)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Introdução aos menus de atalho para objetos do sistema de arquivos

Como os menus de atalho são frequentemente usados para gerenciamento de arquivos, o Shell fornece um conjunto de comandos padrão, como **recortar** e **copiar**, que aparecem no menu de atalho para qualquer objeto do sistema de arquivos, como um arquivo ou uma pasta.

O exemplo a seguir ilustra um menu de atalho padrão exibido ao clicar com o botão direito do mouse em **MyFile.xyz-MS**.

![captura de tela do menu de atalho padrão](images/context-menu/context-filesystemobjects.png)

O motivo pelo qual um menu de atalho padrão é exibido para **MyFile.xyz-MS** é devido ao fato de que **. xyz-MS** não é membro de um tipo de arquivo registrado. Por outro lado, **.txt** é um tipo de arquivo registrado. Se você clicar com o botão direito do mouse em um arquivo de **.txt** , verá um menu de atalho com três comandos adicionais em sua seção superior: **Imprimir**, **Editar** e **abrir com**.

![captura de tela do menu de atalho para um arquivo com um tipo de arquivo registrado](images/context-menu/context-registeredfiletype.png)

Para estender o menu de atalho para um tipo de arquivo, você deve criar uma entrada de registro para cada comando. Uma abordagem mais sofisticada é implementar um manipulador de menu de atalho (verbo), que permite estender o menu de atalho para um tipo de arquivo de acordo com o arquivo. Para obter mais informações, consulte [criando manipuladores de menu de contexto](context-menu-handlers.md)e referência de menu de [contexto](context-menu-reference.md).

### <a name="add-commands-to-a-shortcut-menu"></a>Adicionar comandos a um menu de atalho

Um manipulador de menu de atalho é um manipulador de tipo de arquivo que adiciona comandos a um menu de atalho existente. Os manipuladores de menu de atalho são associados a um tipo de arquivo e são chamados sempre que um menu de atalho é exibido para um membro da classe. O Shell verifica o registro para ver se o tipo de arquivo está associado a qualquer manipulador de menu de atalho. Se for, o Shell consultará os manipuladores para itens de menu de atalho adicionais.

## <a name="shortcut-menu-verbs"></a>Verbos do menu de atalho

Cada comando no menu de atalho é identificado no registro por seu verbo. Esses verbos são os mesmos usados pelo [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ao iniciar aplicativos programaticamente.

Um verbo é uma cadeia de caracteres de texto simples que é usada pelo shell para identificar o comando associado. Cada verbo corresponde à cadeia de caracteres de comando usada para iniciar o comando em uma janela de console ou em um arquivo de lote (.bat).

Por exemplo, o verbo Open normalmente inicia um programa para abrir um arquivo. A cadeia de caracteres de comando geralmente tem a seguinte aparência:


```
"My Program.exe" "%1"
```



Se qualquer elemento da cadeia de caracteres de comando contiver ou puder conter espaços, ele deverá ser colocado entre aspas. Caso contrário, se o elemento contiver um espaço, ele não será analisado corretamente. Por exemplo, **"meu Program.exe"** inicia o aplicativo corretamente. Se você usar **o meu Program.exe** sem aspas, o sistema tentará iniciar **meu** com **Program.exe** como seu primeiro argumento de linha de comando. Você sempre deve usar aspas com argumentos como **"%1**" que são expandidos para cadeias de caracteres pelo shell, pois não é possível ter certeza de que a cadeia de caracteres não conterá um espaço.

Os verbos também podem ter um nome de exibição associado a eles, que é exibido no menu de atalho em vez da própria cadeia de caracteres de verbo. Por exemplo, a cadeia de caracteres de exibição para openas é **aberta com**. Assim como as cadeias de menu normais, a inclusão de um caractere de e comercial na cadeia de caracteres de exibição permite a seleção de teclado do comando.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>transmitir itens de sistema sem arquivos e resultados de OpenSearch.

no Windows 7 e posterior, há suporte para a conexão de fontes externas para o cliente Windows por meio do protocolo [OpenSearch](http://www.opensearch.org/) . isso permite que os usuários pesquisem um armazenamento de dados remoto e exibam os resultados de dentro do Windows Explorer. o padrão OpenSearch v 1.1 define formatos de arquivo simples que podem ser usados para descrever como um cliente deve consultar o serviço web para o armazenamento de dados e como o serviço deve retornar os resultados a serem processados pelo cliente.

talvez seja necessário transmitir itens que não sejam do sistema de arquivos para evitar a necessidade de baixar itens no caso de resultados de [OpenSearch](http://www.opensearch.org/) . o recurso de pesquisa federada permite pesquisar itens de locais de sistema que não são de arquivos que dão suporte a OpenSearch, como SharePoint e outros sites de backup de serviços da web, por exemplo. Ao invocar verbos nesses itens, o sistema baixa uma versão temporária do item e a passa para a implementação do verbo. Os implementadores de verbo são incentivados a evitar a necessidade de baixar o arquivo registrando o conjunto de esquemas de URL que o verbo dá suporte para transmitir os itens. Os verbos fazem isso usando a chave do registro **SupportedProtocols** .

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Registrar um aplicativo para lidar com tipos de arquivo arbitrários

A definição de itens de menu de atalho para um determinado tipo de arquivo permite que você especifique como o aplicativo associado abre um membro do tipo de arquivo. No entanto, os aplicativos também podem registrar um procedimento padrão separado para ser usado quando um usuário tenta usar o aplicativo para abrir um tipo de arquivo que não está associado ao aplicativo. Você registra o procedimento padrão praticamente da mesma maneira que registra itens de menu de atalho. Para obter informações mais detalhadas sobre como definir itens de menu de atalho, consulte [criando manipuladores de menu de contexto](context-menu.md).

O procedimento padrão atende a duas finalidades básicas. Uma é especificar como seu aplicativo deve ser chamado para abrir um tipo de arquivo arbitrário. Você pode, por exemplo, usar um sinalizador de linha de comando para indicar que um tipo de arquivo desconhecido está sendo aberto. A outra finalidade é definir as várias características de um tipo de arquivo, como os itens de menu de atalho e o ícone. Se um usuário associar seu aplicativo a um tipo de arquivo adicional, essa classe terá essas características. Se o tipo de arquivo adicional tiver sido associado anteriormente a outro aplicativo, essas características substituirão os originais.

Para registrar o procedimento padrão, coloque as mesmas chaves do registro que você criou para o ProgID do seu aplicativo na subchave do aplicativo de **\_ \_ \\ aplicativos raiz de classes hKey**. Você também pode incluir um valor de **FriendlyAppName** para fornecer ao sistema um nome amigável para seu aplicativo. O nome amigável do aplicativo também pode ser extraído de seu arquivo executável, mas somente se o valor FriendlyAppName estiver ausente.

A seguinte entrada de registro de exemplo ilustra um procedimento padrão para **MyProgram.exe** que define um nome amigável e vários itens de menu de atalho. As cadeias de caracteres de comando incluem o sinalizador **/a** para notificar o aplicativo de que ele está abrindo um tipo de arquivo arbitrário. Se você incluir uma subchave **DefaultIcon** , deverá usar um ícone genérico.

```
HKEY_CLASSES_ROOT
   MyProgram.exe
      shell
         open
            command
               (Default) = C:\MyDir\MyProgram.exe /a "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2"
```

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter mais informações, consulte [introdução às associações de arquivo](fa-intro.md).
-   Para obter informações conceituais sobre como estender o shell com manipuladores de tipo de arquivo, consulte [criando manipuladores de extensão de shell](handlers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para manipuladores de menu de atalho e verbos de seleção múltipla](verbs-best-practices.md)
</dt> <dt>

[Escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md)
</dt> <dt>

[Como Criar Manipuladores do Menu de Atalho](context-menu-handlers.md)
</dt> <dt>

[Personalizando um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Referência do menu de atalho](context-menu-reference.md)
</dt> </dl>

 

 



