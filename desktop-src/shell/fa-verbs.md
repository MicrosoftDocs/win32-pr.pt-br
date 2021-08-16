---
description: Quando um usuário clica com o botão direito do mouse em um objeto Shell, como um arquivo, o Shell exibe um menu de atalho (contexto).
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

Quando um usuário clica com o botão direito do mouse em um objeto Shell, como um arquivo, o Shell exibe um menu de atalho (contexto). Esse menu contém uma lista de comandos que o usuário pode selecionar para executar várias ações no item. Esses comandos também são conhecidos como itens de menu de atalho ou verbos. Os menus de atalho podem ser personalizados.

Este tópico é organizado da seguinte forma:

-   [Introdução aos menus de atalho para objetos do sistema de arquivos](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [Adicionar comandos a um menu de atalho](#add-commands-to-a-shortcut-menu)
-   [Verbos do menu de atalho](#shortcut-menu-verbs)
-   [Transmitir itens do sistema que não são arquivos e OpenSearch resultados.](#stream-non-file-system-items-and-opensearch-results)
-   [Registrar um aplicativo para lidar com tipos de arquivo arbitrários](#register-an-application-to-handle-arbitrary-file-types)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a>Introdução aos menus de atalho para objetos do sistema de arquivos

Como os menus de atalho geralmente são usados para gerenciamento de arquivos, o Shell fornece um conjunto de comandos padrão, como **Recortar** e **Copiar,** que aparecem no menu de atalho para qualquer objeto do sistema de arquivos, como um arquivo ou uma pasta.

O exemplo a seguir ilustra um menu de atalho padrão exibido clicando com o botão **direito do mouse MyFile.xyz-ms**.

![captura de tela do menu de atalho padrão](images/context-menu/context-filesystemobjects.png)

O motivo pelo qual um menu de atalho padrão é **exibido para MyFile.xyz-ms** é devido ao fato de **que .xyz-ms** não é membro de um tipo de arquivo registrado. Por outro lado, **.txt** é um tipo de arquivo registrado. Se você clicar com o botão direito do mouse em um **arquivo.txt,** verá  um menu de atalho com três comandos adicionais em sua seção superior: **Imprimir,** Editar **e Abrir com**.

![captura de tela do menu de atalho para um arquivo com um tipo de arquivo registrado](images/context-menu/context-registeredfiletype.png)

Para estender o menu de atalho para um tipo de arquivo, você deve criar uma entrada do Registro para cada comando. Uma abordagem mais sofisticada é implementar um manipulador de menu de atalho (verbo), que permite estender o menu de atalho para um tipo de arquivo em uma base de arquivo por arquivo. Para obter mais informações, consulte [Criando manipuladores de menu de contexto](context-menu-handlers.md)e Referência de menu de [contexto](context-menu-reference.md).

### <a name="add-commands-to-a-shortcut-menu"></a>Adicionar comandos a um menu de atalho

Um manipulador de menu de atalho é um manipulador de tipo de arquivo que adiciona comandos a um menu de atalho existente. Manipuladores de menu de atalho são associados a um tipo de arquivo e são chamados sempre que um menu de atalho é exibido para um membro da classe . O Shell verifica o Registro para ver se o tipo de arquivo está associado a qualquer manipulador de menu de atalho. Se estiver, o Shell consultará os manipuladores em busca de itens de menu de atalho adicionais.

## <a name="shortcut-menu-verbs"></a>Verbos do menu de atalho

Cada comando no menu de atalho é identificado no Registro por seu verbo. Esses verbos são os mesmos usados pelo [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ao iniciar aplicativos programaticamente.

Um verbo é uma cadeia de caracteres de texto simples usada pelo Shell para identificar o comando associado. Cada verbo corresponde à cadeia de caracteres de comando usada para iniciar o comando em uma janela do console ou arquivo .bat lote.

Por exemplo, o verbo aberto normalmente inicia um programa para abrir um arquivo. A cadeia de caracteres de comando normalmente tem a seguinte aparência:


```
"My Program.exe" "%1"
```



Se qualquer elemento da cadeia de caracteres de comando contiver ou contiver espaços, ele deverá ser entre aspas. Caso contrário, se o elemento contiver um espaço, ele não será analisado corretamente. Por exemplo, **"Meu Program.exe"** inicia o aplicativo corretamente. Se você usar **Meu Program.exe** sem aspas, o sistema tentará iniciar My **com** Program.exe **como** seu primeiro argumento de linha de comando. Você sempre deve usar aspas com argumentos como **"%1"** que são expandidos para cadeias de caracteres pelo Shell, porque não é possível ter certeza de que a cadeia de caracteres não conterá um espaço.

Os verbos também podem ter um nome de exibição associado a eles, que é exibido no menu de atalho em vez da própria cadeia de caracteres de verbo. Por exemplo, a cadeia de caracteres de exibição para openas **é Abrir com**. Como cadeias de caracteres de menu normais, incluindo um caractere de e ampersand na cadeia de caracteres de exibição permite a seleção do teclado do comando.

## <a name="stream-non-file-system-items-and-opensearch-results"></a>Transmitir itens do sistema que não são arquivos e OpenSearch resultados.

No Windows 7 e posterior, há suporte para a conexão de fontes externas com o Windows Client por meio do [protocolo OpenSearch.](http://www.opensearch.org/) Isso permite que os usuários pesquisem um armazenamento de dados remoto e vejam os resultados de dentro Windows Explorer. O padrão OpenSearch v1.1 define formatos de arquivo simples que podem ser usados para descrever como um cliente deve consultar o serviço Web para o armazenamento de dados e como o serviço deve retornar resultados a serem renderizados pelo cliente.

Talvez seja necessário transmitir itens que não são do sistema de arquivos para evitar a necessidade de baixar itens no caso [de](http://www.opensearch.org/) OpenSearch resultados. O recurso de pesquisa federada permite pesquisar itens de locais que não são do sistema de arquivos que suportam OpenSearch, como SharePoint e outros sites com suporte de serviços Web, por exemplo. Ao invocar verbos nesses itens, o sistema baixa uma versão temporária do item e a passa para a implementação do verbo. Os implementadores verbais são incentivados a evitar a necessidade de baixar o arquivo registrando o conjunto de esquemas de URL compatíveis com o verbo para transmitir os itens. Os verbos fazem isso usando a chave do Registro **SupportedProtocols.**

## <a name="register-an-application-to-handle-arbitrary-file-types"></a>Registrar um aplicativo para lidar com tipos de arquivo arbitrários

Definir itens de menu de atalho para um tipo de arquivo específico permite que você especifique como o aplicativo associado abre um membro do tipo de arquivo. No entanto, os aplicativos também podem registrar um procedimento padrão separado a ser usado quando um usuário tenta usar o aplicativo para abrir um tipo de arquivo que não está associado ao aplicativo. Registre o procedimento padrão da mesma maneira que registra itens de menu de atalho. Para obter informações mais detalhadas sobre como definir itens de menu de atalho, consulte [Criando manipuladores de menu de contexto.](context-menu.md)

O procedimento padrão atende a duas finalidades básicas. Uma delas é especificar como seu aplicativo deve ser invocado para abrir um tipo de arquivo arbitrário. Você pode, por exemplo, usar um sinalizador de linha de comando para indicar que um tipo de arquivo desconhecido está sendo aberto. A outra finalidade é definir as várias características de um tipo de arquivo, como os itens de menu de atalho e o ícone. Se um usuário associar seu aplicativo a um tipo de arquivo adicional, essa classe terá essas características. Se o tipo de arquivo adicional tiver sido associado anteriormente a outro aplicativo, essas características substituirão os originais.

Para registrar o procedimento padrão, coloque as mesmas chaves do Registro que você criou para o ProgID do aplicativo na sub-chave do aplicativo de Aplicativos RAIZ **HKEY \_ CLASSES \_ \\**. Você também pode incluir um **valor FriendlyAppName** para fornecer ao sistema um nome amigável para seu aplicativo. O nome amigável do aplicativo também pode ser extraído de seu arquivo executável, mas somente se o valor FriendlyAppName estiver ausente.

A entrada de registro de exemplo a seguir ilustra um procedimento padrão **para** MyProgram.exeque define um nome amigável e vários itens de menu de atalho. As cadeias de caracteres de comando incluem **o sinalizador /a** para notificar o aplicativo de que ele está abrindo um tipo de arquivo arbitrário. Se você incluir uma sub-chave **DefaultIcon,** deverá usar um ícone genérico.

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

-   Para obter informações adicionais, [consulte Introdução às Associações de Arquivos](fa-intro.md).
-   Para obter informações conceituais sobre como estender o Shell com manipuladores de tipo de arquivo, consulte [Criando manipuladores de extensão do Shell.](handlers.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Práticas recomendadas para manipuladores de menu de atalho e vários verbos de seleção](verbs-best-practices.md)
</dt> <dt>

[Escolhendo um verbo estático ou dinâmico para o menu de atalho](shortcut-choose-method.md)
</dt> <dt>

[Como Criar Manipuladores do Menu de Atalho](context-menu-handlers.md)
</dt> <dt>

[Personalização de um menu de atalho usando verbos dinâmicos](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus de atalho (contexto) e manipuladores de menu de atalho](context-menu.md)
</dt> <dt>

[Referência de menu de atalho](context-menu-reference.md)
</dt> </dl>

 

 



