---
description: Demonstra como implementar uma extensão de namespace de Shell, incluindo o comportamento do menu de contexto e tarefas personalizadas no navegador.
title: Exemplo de provedor de dados do Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 31e1d42e4660e0e73830876cfdeb0a5c8a5957cd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471882"
---
# <a name="explorer-data-provider-sample"></a>Exemplo de provedor de dados do Explorer

Demonstra como implementar uma extensão de namespace de Shell, incluindo o comportamento do menu de contexto e tarefas personalizadas no navegador.

Este tópico inclui as seções a seguir.

-   [Requisitos](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Location      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de ExplorerDataProvider](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **ExplorerDataProvider** .
2.  Digite `msbuild ExplorerDataProvider.sln`.

para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  abra Windows Explorer e navegue até o diretório do projeto **ExplorerDataProvider** .
2.  Clique duas vezes no ícone do arquivo ExplorerDataProvider. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**. A DLL será criada no diretório padrão de \\ depuração ou de \\ liberação.

> [!Note]  
> na versão deste exemplo incluída no SDK do Windows, a configuração para a compilação de versão de 64 bits não inclui o arquivo ExplorerDataProvider. def na opção de **arquivo de definição de módulo** do vinculador. Você deve especificar esse arquivo antes de Compilar em um ambiente de 64 bits. Adicione a linha `ModuleDefinitionFile="ExplorerDataProvider.def"` à seção VCLinkerTool (começa na linha 329) do arquivo ExplorerDataProvider. vcproj, como mostrado aqui:
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>LinkIncremental="1"&gt; AdditionalLibraryDirectories=""c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64""&gt; ModuleDefinitionFile="ExplorerDataProvider.def"&gt; GenerateDebugInformation="true"</code></pre> | 

>
> 
>
> A versão deste exemplo baixável da Galeria de códigos foi corrigida para esse problema e nenhuma ação extra é necessária em sua parte.
>
>  
>
> ## <a name="running-the-sample"></a>Executando o exemplo
>
> 1.  navegue até o diretório que contém o novo arquivo .dll e. propdesc, usando o prompt de comando ou o gerenciador de Windows.
> 2.  Na linha de comando, digite `regsvr32.exe` .
>     > [!Note]  
>     > Se você executar esse comando em um prompt de comando elevado, o registro automático também registrará o arquivo. propDesc automaticamente. Se ele for executado de um prompt de comando sem privilégios elevados, a extensão do namespace funcionará, mas sem a funcionalidade de propriedade personalizada.
>
>      
>
> 3.  Abra a pasta **meu computador** e procure a nova extensão de namespace presente nela.
>
>  
>
>  
>


