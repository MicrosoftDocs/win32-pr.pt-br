---
description: O redirecionamento de DLL/COM é uma estratégia de isolamento de aplicativo empregada por administradores corporativos no Windows XP.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Redirecionamento de DLL/COM no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e356c7b4cc6e5616a03eba60439c7478d65e626a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829464"
---
# <a name="dllcom-redirection-on-windows"></a>Redirecionamento de DLL/COM no Windows

O redirecionamento de DLL/COM é uma estratégia de isolamento de aplicativo empregada por administradores corporativos no Windows XP.

* * Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP com SP2: * * o uso de estratégias de redirecionamento de DLL/COM não é recomendado porque aplicativos isolados que usam manifestos e [assemblies lado a lado](about-side-by-side-assemblies-.md) podem ser mais fáceis de atualizar e atender. A presença de um arquivo. local será ignorada se um manifesto estiver presente. A estratégia de redirecionamento de DLL/COM usando arquivos. local funciona se o aplicativo não tiver um manifesto.

O redirecionamento de DLL/COM associa um aplicativo a uma versão local de um componente. Os arquivos do componente local podem ser mantidos separados da versão do componente do sistema em um local que seja privado para o aplicativo. A versão do sistema do componente é registrada globalmente e disponível para outros aplicativos que se associam a ele. A versão local do componente é reservada para o uso exclusivo do aplicativo. Se necessário, os arquivos de componente usados pelo aplicativo podem ser carregados na memória ao mesmo tempo que os arquivos de componente do sistema.

A redirecionamento de DLL/COM é ativada pela instalação de um arquivo especial juntamente com uma cópia do arquivo de componente local no mesmo diretório que o arquivo executável do aplicativo. O arquivo especial é um arquivo vazio chamado após o nome do arquivo executável do aplicativo e acrescentado com. local. Por exemplo, para ativar o redirecionamento de DLL/COM para um aplicativo chamado MyApp, a versão local do componente e um arquivo vazio chamado Myapp.exe. local devem ser copiados para a pasta que contém Myapp.exe. Isso associa o aplicativo à versão local do componente em vez da versão compartilhada globalmente do componente.

Quando um aplicativo carrega um arquivo de componente, como um arquivo DLL ou. ocx, o Windows primeiro o procura na pasta em que o arquivo. local e executável do aplicativo está instalado. Se for encontrado, o aplicativo usará esse arquivo de componente, independentemente de qualquer caminho de pesquisa de diretório definido no aplicativo ou no registro. Se não for encontrado, o arquivo de componente no caminho de pesquisa definido será usado.

O utilitário de instalação do deve fazer o seguinte para instalar o aplicativo com o redirecionamento de DLL/COM:

-   Um arquivo. local vazio deve ser copiado para a mesma pasta que o arquivo executável do aplicativo.
-   Todos os componentes, DLL e arquivos. ocx usados pelo aplicativo devem ser copiados para a mesma pasta que o arquivo executável do aplicativo.
-   Os componentes COM isolados devem ser registrados com o Windows para que diferentes versões do assembly não entrem em conflito entre si quando são carregadas na memória ao mesmo tempo. O processo de registro requer que, enquanto a implementação do componente pode ser alterada entre versões, determinados metadados COM como CLSID, ProgID, biblioteca de tipos e modelo de threading não podem.
-   Se o aplicativo for instalado usando o Windows Installer, o diretório do aplicativo poderá ser protegido usando a Tabela LockPermissions. Normalmente, o sistema recebe acesso de leitura, gravação e execução; todos os outros processos recebem apenas acesso de execução e leitura.

 

 



