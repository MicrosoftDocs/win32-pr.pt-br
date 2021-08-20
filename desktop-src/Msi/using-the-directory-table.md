---
description: A tabela de diretórios especifica o layout de uma instalação do.
ms.assetid: 3f2e1cc2-6b36-4615-86e6-e78485edd2f7
title: Usando a tabela de diretórios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f550f32006df16db5811e0fbf5022253373a4b1551983ddda2db55655b4061f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141315"
---
# <a name="using-the-directory-table"></a>Usando a tabela de diretórios

A [tabela de diretórios](directory-table.md) especifica o layout de uma instalação do. Quando os diretórios são resolvidos durante a [ação CostFinalize](costfinalize-action.md), as chaves na tabela de diretórios tornam-se [Propriedades](properties.md) definidas como caminhos de diretório. Observe que o instalador define um número de [Propriedades](properties.md) padrão para caminhos de pasta do sistema. Consulte a [referência de propriedade](property-reference.md) para obter uma lista das propriedades definidas como pastas do sistema.

A melhor maneira de especificar o local de destino de um diretório é criando a [tabela de diretórios](directory-table.md) no seu pacote de instalação para fornecer o local correto, conforme discutido nesta seção. Se for necessário alterar o local do diretório no momento da instalação, consulte também a seção: [alterando o local de destino de um diretório](changing-the-target-location-for-a-directory.md)

Veja a seguir um exemplo de uma tabela de diretórios.



| Diretório     | Pai do diretório \_ | DefaultDir |
|---------------|-------------------|------------|
| TARGETDIR     |                   | SourceDir  |
| EXEDIR        | TARGETDIR         | Aplicativo        |
| DLLDIR        | EXEDIR            | Compartimento        |
| DesktopFolder | TARGETDIR         | Desktop    |



 

Cada linha da tabela de diretório indica um diretório na origem e no destino. Por exemplo, suponha que o pacote de instalação resida na \\ \\ origem dos aplicativos \\ \\ . Como o \_ campo pai do diretório da primeira linha é nulo, esse registro indica os diretórios raiz para a origem e o destino. Para a origem, o valor desse diretório é fornecido pelo campo DefaultDir. A propriedade [**SourceDir**](sourcedir.md) assume como padrão o local do pacote de instalação. Portanto, a menos que a propriedade **SourceDir** seja substituída, o diretório de origem raiz é \\ \\ Applications \\ \\ .

O campo Directory do primeiro registro indica o local do diretório de destino raiz. Nesse caso, o valor da propriedade [**TARGETDIR**](targetdir.md) indica esse diretório. Normalmente, o valor da propriedade **TARGETDIR** é definido na linha de comando ou por meio de uma interface do usuário. Nesse caso, suponha que a propriedade **TARGETDIR** esteja definida como C: \\ arquivos de programa \\ destino \\ .

Para o segundo registro, o \_ campo pai do diretório não é nulo. Portanto, esse registro indica um diretório não raiz para a origem e o destino. Para um diretório de origem não raiz, o diretório de origem indicado pelo registro descrito no \_ campo pai do diretório é o diretório pai. Para o segundo registro, o \_ campo pai do diretório é TARGETDIR. Conforme mostrado anteriormente, o diretório de origem indicado pelo registro TARGETDIR resolvido para a \\ \\ origem dos aplicativos \\ \\ . Assim, o diretório de origem indicado pelo segundo registro é \\ \\ aplicativo de origem de aplicativos \\ \\ \\ .

Um processo semelhante funciona para o diretório de destino. O valor do diretório pai para o diretório de destino descrito no segundo registro é o diretório de destino resolvido pelo \_ campo pai do diretório. Novamente, o \_ campo pai do diretório contém o valor TARGETDIR. Isso indica o primeiro registro que é resolvido para um diretório de destino do destino de \\ arquivos de programas C: \\ \\ . O campo diretório contém uma propriedade definida pelo autor chamada EXEDIR. Se essa propriedade for definida, seu valor fornecerá o caminho completo do diretório. Portanto, se essa propriedade for definida como C: \\ Data \\ Common \\ , o valor do diretório de destino indicado pelo segundo registro será C: \\ Data \\ Common \\ . Se não estiver definido, o diretório de destino usará o nome fornecido pelo campo DefaultDir. Nesse caso, o diretório de destino é C: \\ arquivos de programas de \\ destino \\ aplicativo \\ .

O mesmo processo funciona para o terceiro registro. Se EXEDIR e DLLDIR não estiverem definidos, o diretório de destino será C: \\ arquivos de programas \\ destino \\ app \\ bin e o diretório de origem é \\ \\ \\ app Application Source \\ \\ bin \\ .

O quarto registro usa a propriedade [**DesktopFolder**](desktopfolder.md) . Se o local da área de trabalho do usuário for C: \\ WinNT \\ perfis \\ user \\ Desktop \\ , o diretório de destino será resolvido para C: \\ WinNT \\ perfis \\ user \\ Desktop \\ . O diretório de origem é resolvido para a \\ \\ área de trabalho de origem de aplicativos \\ \\ \\ .

Há dois recursos de sintaxe adicionais que podem ser usados na coluna DefaultDir da tabela de diretórios. Para um diretório de origem não raiz, um ponto (.) inserido na coluna DefaultDir indica que o diretório deve estar localizado em seu diretório pai sem um subdiretório. Para especificar caminhos de diretório de origem e de destino diferentes, separe os caminhos de destino e de origem na coluna DefaultDir com dois-pontos da seguinte maneira: \[ TargetPath \] : \[ SourcePath \] . Esses recursos podem ser usados juntos para adicionar níveis aos caminhos de origem ou de destino de um único diretório. Consulte o exemplo a seguir de uma tabela de diretórios.



| Diretório   | Pai do diretório \_ | DefaultDir |
|-------------|-------------------|------------|
| TARGETDIR   |                   | SourceDir  |
| MyAppDir    | TARGETDIR         | MyApp      |
| BinDir      | MyAppDir          | Compartimento        |
| Binx86Dir   | BinDir            | .: x86      |
| BinAlphaDir | BinDir            | .: Alfa    |



 

Os caminhos de origem e de destino são resolvidos para as linhas MyAppDir, BinDir, Binx86Dir e BinAlphaDir da seguinte maneira.



| Record       | Caminhos de destino            | Caminhos de origem                   |
|--------------|-------------------------|--------------------------------|
| MyAppDir:    | \[TARGETDIR \] MyApp      | \[MyApp de SourceDir \]             |
| BinDir:      | \[\]Compartimento TARGETDIR MyApp \\ | \[\]Compartimento MyApp de SourceDir \\        |
| Binx86Dir:   | \[\]Compartimento TARGETDIR MyApp \\ | \[\]Escaninho MyApp de SourceDir \\ \\ x86   |
| BinAlphaDir: | \[\]Compartimento TARGETDIR MyApp \\ | \[\]Alpha de \\ compartimento \\ MyApp de SourceDir |



 

> [!Note]  
> a plataforma Alpha não é suportada pelo Windows Installer.

 

 

 



