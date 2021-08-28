---
description: Demonstra como implementar uma extensão de namespace do Shell, incluindo o comportamento do menu de contexto e tarefas personalizadas no navegador.
title: Exemplo de provedor de dados do Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b30a1c6cb31038d69c9feb85f0382fd5f4bb89bf
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786702"
---
# <a name="explorer-data-provider-sample"></a>Exemplo de provedor de dados do Explorer

Demonstra como implementar uma extensão de namespace do Shell, incluindo o comportamento do menu de contexto e tarefas personalizadas no navegador.

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

| Local      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de ExplorerDataProvider](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo no prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **ExplorerDataProvider.**
2.  Digite `msbuild ExplorerDataProvider.sln`.

Para criar o exemplo usando Microsoft Visual Studio (preferencial):

1.  Abra Windows Explorer e navegue até o diretório do projeto **ExplorerDataProvider.**
2.  Clique duas vezes no ícone do arquivo ExplorerDataProvider.sln para abrir o projeto Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**. A DLL será criada no diretório \\ Padrão de Depuração \\ ou Versão.

> [!Note]  
> Na versão deste exemplo incluída no SDK do Windows, a configuração para o build de versão de 64 bits não inclui  o arquivo ExplorerDataProvider.def na opção Arquivo de Definição de Módulo do vinculador. Você deve especificar esse arquivo por conta própria antes de criar em um ambiente de 64 bits. Adicione a linha `ModuleDefinitionFile="ExplorerDataProvider.def"` à seção VCLinkerTool (começa na linha 329) do arquivo ExplorerDataProvider.vcproj, conforme mostrado aqui:
>
> 
>
> 
| | | <pre><code>LinkIncremental="1"&gt; AdditionalLibraryDirectories=""c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64""&gt; ModuleDefinitionFile="ExplorerDataProvider.def"&gt; GenerateDebugInformation="true"</code></pre> | 

>
> 
>
> A versão deste exemplo que pode ser baixada da Galeria de Códigos foi corrigida para esse problema e nenhuma ação extra é necessária da sua parte.
>
>  
>
> ## <a name="running-the-sample"></a>Executando o exemplo
>
> 1.  Navegue até o diretório que contém os novos arquivos .dll e .propdesc, usando o prompt de comando ou Windows Explorer.
> 2.  Na linha de comando, digite `regsvr32.exe` .
>     > [!Note]  
>     > Se você executar esse comando em um prompt de comando com elevação, o autoregiso também registrará o arquivo .propdesc automaticamente. Se for executado em um prompt de comando não elevado, a extensão de namespace funcionará, mas sem a funcionalidade de propriedade personalizada.
>
>      
>
> 3.  Abra a **Meu Computador** e procure a nova extensão de namespace presente lá.
>
>  
>
>  
>


