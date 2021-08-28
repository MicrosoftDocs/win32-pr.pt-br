---
title: Como usar o Visual Studio
description: Para sua conveniência, Microsoft Visual Studio 6.0 fornece um arquivo de projeto para cada exemplo.
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee6edc1b19cb0e56495c8af6f96d28e4d255e40d53161671f52a1a7d27939f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796846"
---
# <a name="using-visual-studio"></a>Como usar o Visual Studio

Para sua conveniência, Microsoft Visual Studio 6.0 fornece um arquivo de projeto para cada exemplo. Esse arquivo tem a extensão DSP. Um arquivo de workspace Allsamp.dsw também é fornecido no diretório principal para que você possa compilar todos os exemplos de uma vez de dentro Visual Studio.

> [!Note]  
> As instruções a seguir são escritas para Microsoft Visual Studio 6.0. Os comandos podem ser diferentes em versões anteriores e posteriores do Visual Studio.

 

Para carregar o projeto apropriado para um exemplo, você pode executar Visual Studio no prompt de comando no diretório do exemplo, conforme mostrado no exemplo a seguir. Você deve substituir o nome do projeto de exemplo para **<project name>** .

**msdev <project name> .dsp**

Você também pode simplesmente clicar duas vezes no arquivo .dsp no Windows Explorer para carregar o workspace de um exemplo no Visual Studio. De dentro Visual Studio você pode procurar as classes C++ da origem de exemplo e geralmente executar as outras operações edit-compile-debug.

Como parte do SDK (Kit de Desenvolvimento de Software de Plataforma), a compilação desses exemplos de dentro do Visual Studio requer a configuração adequada dos caminhos de diretório no Visual Studio. Para definir os caminhos de diretório, execute as seguintes etapas:

-   Execute Microsoft Visual Studio (Visual C++).
-   Escolha **Opções...** **no** menu Ferramentas.
-   Escolha a **guia Diretórios** na caixa **de diálogo** Opções.
-   Na  lista drop-down Mostrar Diretórios  para, selecione Arquivos executáveis e insira o caminho do diretório BIN para o SDK da Plataforma instalado (por exemplo, C: Arquivos de Programas Compartimento do \\ \\ SDK da \\ Microsoft). Clique no botão de seta para cima para mover esse caminho inserido recentemente para que ele seja a primeira entrada na **lista Diretórios.**
-   Na lista **drop-down** Mostrar Diretórios para, selecione Incluir arquivos e insira o caminho do diretório INCLUDE para o SDK da Plataforma instalado (por exemplo, C: Arquivos de Programas Microsoft  \\ \\ SDK \\ incluem). Clique no botão de seta para cima para mover esse caminho inserido recentemente para que ele seja a primeira entrada na **lista Diretórios.**
-   Na lista **drop-down** Mostrar Diretórios para, selecione Arquivos de biblioteca e insira o caminho do diretório LIB para o SDK da Plataforma instalado (por exemplo, C: Arquivos de Programas Microsoft  \\ \\ SDK \\ Lib). Clique nos botões de seta para cima para mover esse caminho inserido recentemente para que ele seja a primeira entrada na **lista Diretórios.**
-   Clique no botão OK na caixa **de diálogo Opções** para concluir as configurações.

A partir daí, você pode usar o editor, o depurador e os recursos do projeto para editar, compilar, vincular e depurar.

Outros IDEs visuais também podem gerar facilmente um de seus makefiles de projeto nativo, considerando os arquivos de origem existentes de um exemplo de código. Se você estiver usando um IDE desse tipo, gerar um makefile de projeto nativo desse tipo pode valer a pena, pois oferece uma maneira de procurar as classes C++ do programa. Para obter mais informações sobre como usar makefiles externos ou criar um makefile de projeto nativo usando um conjunto de arquivos de origem existentes, consulte a documentação do IDE.

Além da dependência do código comum nos diretórios IRMÃOS APPUTIL, INC e LIB, muitos exemplos de código são autossu contidos. Crie APPUTIL antes de criar outros exemplos de código. Alguns exemplos posteriormente na sequência podem funcionar com os resultados compilados de exemplos anteriores. Estas interdependências de exemplo de código são as seguinte:

-   Qualquer: o build de qualquer exemplo de código precisa de build anterior do APPUTIL.
-   DLLUSER: criar ou executar precisa de build anterior de DLLSKEL.
-   COMUSER: a com build ou a executar precisa de build anterior do COMOBJ.
-   DLLSERVE: o build precisa de build anterior de REGISTER.
-   DLLCL LTD: a executar precisa de build anterior de DLLSERVE.
-   LICSERVE: o build precisa de build anterior de REGISTER.
-   LICCL LTD: a executar precisa de build anterior de LICSERVE e DLLSERVE.
-   MARSHAL: o build precisa de build anterior de REGISTER.
-   LOCSERVE: a com build ou a executar precisa de build anterior de REGISTER e MARSHAL.
-   LOCCLIEN: a executar precisa de build anterior do LOCSERVE.
-   APTSERVE: a com build ou a executar precisa de build anterior de REGISTER e MARSHAL.
-   APTCL LTDA: a executar precisa de build anterior do APTSERVE.
-   REMCL LTDA: o build ou a executar precisa de build anterior de REGISTER e MARSHAL no computador local (cliente). Executar precisa de build anterior de REGISTER, MARSHAL e APTSERVE no computador remoto (servidor).
-   FRESERVE: o build precisa de build anterior de REGISTER.
-   FRECL LTD: a executar precisa de build anterior de FRESERVE.
-   CONSERVE: o build precisa de build anterior de REGISTER.
-   CONCLIEN: a executar precisa de build anterior do CONSERVE.
-   STOSERVE: o build precisa de build anterior de REGISTER.
-   STOCL LTD: a executar precisa de build anterior do STOSERVE.
-   PERSERVE: o build precisa de build anterior de REGISTER.
-   PERTEXT: o build precisa de build anterior de REGISTER.
-   PERDRAW: o build precisa de build anterior de REGISTER.
-   PERCL LTDA: a run precisa de build anterior de PERSERVE, PERTEXT e PERDRAW.
-   DCDMARSH: o build precisa de build anterior de REGISTER.
-   DCDSERVE: criar ou executar precisa de build anterior de REGISTER e DCDMARSH.
-   DCOMDRAW: criar ou executar precisa de build anterior de REGISTER e DCDMARSH no computador local (cliente). Executar precisa de build anterior de REGISTER, DCDMARSH e DCOMDRAW no computador remoto (servidor).

 

 




