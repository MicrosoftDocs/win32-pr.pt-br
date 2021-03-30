---
title: Como usar o Visual Studio
description: Para sua conveniência, Microsoft Visual Studio 6,0 fornece um arquivo de projeto para cada exemplo.
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b32359a29d14a6cd5a4d08d015a6598ade376d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634833"
---
# <a name="using-visual-studio"></a>Como usar o Visual Studio

Para sua conveniência, Microsoft Visual Studio 6,0 fornece um arquivo de projeto para cada exemplo. Esse arquivo tem a extensão DSP. Um arquivo de espaço de trabalho de domínio \ SAMP. DSW também é fornecido no diretório principal para que você possa compilar todos os exemplos de uma vez no Visual Studio.

> [!Note]  
> As instruções a seguir são gravadas para o Microsoft Visual Studio 6,0. Os comandos podem diferir em versões anteriores e posteriores do Visual Studio.

 

Para carregar o projeto apropriado para um exemplo, você pode executar o Visual Studio no prompt de comando no diretório de exemplo, conforme mostrado no exemplo a seguir. Você deve substituir o nome do projeto de exemplo para **<project name>** .

**Msdev <project name> . Dsp**

Você também pode simplesmente clicar duas vezes no arquivo. Dsp no Windows Explorer para carregar um espaço de trabalho de exemplo no Visual Studio. No Visual Studio, você pode navegar pelas classes C++ da fonte de exemplo e, geralmente, executar as outras operações de edição-compilação-depuração.

Como parte do SDK (Kit de desenvolvimento de software) da plataforma, a compilação desses exemplos de dentro do Visual Studio requer a configuração apropriada dos caminhos de diretório no Visual Studio. Para definir os caminhos de diretório, execute as seguintes etapas:

-   Execute Microsoft Visual Studio (Visual C++).
-   Escolha **opções...** no menu **ferramentas** .
-   Escolha a guia **diretórios** na caixa de diálogo **Opções** .
-   Na lista suspensa **Mostrar diretórios para** , selecione **arquivos executáveis** e insira o caminho do diretório bin para o SDK da plataforma instalado (por exemplo, C: \\ arquivos de programas \\ Microsoft SDK \\ bin). Clique no botão de seta para cima para mover esse caminho inserido recentemente para que ele seja a primeira entrada na lista de **diretórios** .
-   Na lista suspensa **Mostrar diretórios para** , selecione **incluir arquivos** e insira o caminho do diretório de inclusão para o SDK da plataforma instalada (por exemplo, C: \\ arquivos de programas \\ Microsoft SDK \\ inclui). Clique no botão de seta para cima para mover esse caminho inserido recentemente para que ele seja a primeira entrada na lista de **diretórios** .
-   Na lista suspensa **Mostrar diretórios para** , selecione arquivos de **biblioteca** e insira o caminho do diretório lib para o SDK da plataforma instalado (por exemplo, C: \\ arquivos de programas \\ Microsoft SDK \\ lib). Clique nos botões de seta para cima para mover esse caminho inserido recentemente para que ele seja a primeira entrada na lista de **diretórios** .
-   Clique no botão OK na caixa de diálogo **Opções** para concluir as configurações.

A partir daí, você pode usar o editor, o depurador e os recursos do projeto para editar, compilar, vincular e depurar.

Outros IDEs visuais também podem gerar facilmente um de seus makefiles de projeto nativo, considerando os arquivos de origem existentes de um exemplo de código. Se você estiver usando um IDE, gerar tal Makefile de projeto nativo pode ser muito útil porque oferece uma maneira de procurar as classes C++ do programa. Para obter mais informações sobre como usar Makers externos ou como criar um makefile de projeto nativo usando um conjunto de arquivos de origem existentes, consulte a documentação do IDE.

Além da dependência do código comum nos diretórios irmãos APPUTIL, INC e LIB, muitos exemplos de código são independentes. Crie APPUTIL antes de criar outros exemplos de código. Alguns exemplos mais tarde na sequência podem funcionar com os resultados compilados de amostras anteriores. Essas interdependências de exemplo de código são as seguintes:

-   Qualquer: a compilação de qualquer exemplo de código precisa de uma compilação anterior de APPUTIL.
-   DLLUSER: a compilação ou execução precisa de uma compilação anterior de DLLSKEL.
-   Comuser: a compilação ou execução precisa de uma compilação anterior de COMOBJ.
-   DLLSERVE: a compilação precisa de uma compilação anterior do registro.
-   DLLCLIEN: a execução precisa de uma compilação anterior de DLLSERVE.
-   LICSERVE: a compilação precisa de uma compilação anterior do registro.
-   LICCLIEN: a execução precisa de uma compilação anterior de LICSERVE e DLLSERVE.
-   MARSHAL: as necessidades de compilação antes da compilação do registro.
-   LOCSERVE: a compilação ou execução precisa de uma compilação anterior de registro e MARSHAL.
-   LOCCLIEN: a execução precisa de uma compilação anterior de LOCSERVE.
-   APTSERVE: a compilação ou execução precisa de uma compilação anterior de registro e MARSHAL.
-   APTCLIEN: a execução precisa de uma compilação anterior de APTSERVE.
-   REMCLIEN: a compilação ou execução precisa de uma compilação anterior de registro e MARSHAL no computador local (cliente). As necessidades de execução antes da compilação de registro, MARSHAL e APTSERVE no computador remoto (servidor).
-   FRESERVE: a compilação precisa de uma compilação anterior do registro.
-   FRECLIEN: a execução precisa de uma compilação anterior de FRESERVE.
-   CONSERVAR: a compilação precisa de uma compilação anterior do registro.
-   CONCLIEN: a execução precisa de uma compilação anterior de conservar.
-   STOSERVE: a compilação precisa de uma compilação anterior do registro.
-   STOCLIEN: a execução precisa de uma compilação anterior de STOSERVE.
-   Persirva: a compilação precisa de uma compilação anterior do registro.
-   Pertext: a compilação precisa de uma compilação anterior do registro.
-   Prodraw: a compilação precisa de uma compilação anterior do registro.
-   PERCLIEN: a execução precisa de uma compilação anterior de perpreserve, pertext e o prodraw.
-   DCDMARSH: a compilação precisa de uma compilação anterior do registro.
-   DCDSERVE: a compilação ou execução precisa de uma compilação anterior de REGISTER e DCDMARSH.
-   DCOMDRAW: a compilação ou execução precisa de uma compilação anterior de REGISTER e DCDMARSH no computador local (cliente). A execução precisa de uma compilação anterior de REGISTER, DCDMARSH e DCOMDRAW no computador remoto (servidor).

 

 




