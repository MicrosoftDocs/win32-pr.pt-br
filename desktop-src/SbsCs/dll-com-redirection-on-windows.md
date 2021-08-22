---
description: O redirecionamento de DLL/COM é uma estratégia de isolamento de aplicativo empregada por administradores corporativos no Windows XP.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Redirecionamento de DLL/COM Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ce6b55c2a66d298b7b80248613eab7cefe96c25f8f53dd9218966e235ea267f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142259"
---
# <a name="dllcom-redirection-on-windows"></a>Redirecionamento de DLL/COM Windows

O redirecionamento de DLL/COM é uma estratégia de isolamento de aplicativo empregada por administradores corporativos no Windows XP.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP com SP2: ** O uso de estratégias de redirecionamento DLL/COM não é recomendado porque aplicativos isolados que usam manifestos e [assemblies](about-side-by-side-assemblies-.md) lado a lado podem ser mais fáceis de atualizar e fazer serviço. A presença de um arquivo .local será ignorada se um manifesto estiver presente. A estratégia de redirecionamento de DLL/COM usando arquivos .local funcionará se o aplicativo não tiver um manifesto.

O redirecionamento de DLL/COM vincula um aplicativo a uma versão local de um componente. Os arquivos do componente local podem ser mantidos separados da versão do componente do sistema em um local privado para o aplicativo. A versão do sistema do componente é registrada globalmente e está disponível para todos os outros aplicativos que se vinculam a ele. A versão local do componente é reservada para uso exclusivo do aplicativo. Se necessário, os arquivos de componente usados pelo aplicativo podem ser carregados na memória ao mesmo tempo que os arquivos de componente do sistema.

O redirecionamento de DLL/COM é ativado instalando um arquivo especial junto com uma cópia do arquivo de componente local no mesmo diretório que o arquivo executável do aplicativo. O arquivo especial é um arquivo vazio chamado após o nome do arquivo do executável do aplicativo e anexado com .local. Por exemplo, para ativar o redirecionamento DLL/COM para um aplicativo chamado Myapp, a versão local do componente e um arquivo vazio chamado Myapp.exe.local devem ser copiados para a pasta que contém Myapp.exe. Isso vincula o aplicativo à versão local do componente em vez da versão compartilhada globalmente do componente.

Quando um aplicativo carrega um arquivo de componente, como um arquivo DLL ou .ocx, o Windows primeiro o pesquisa na pasta em que o arquivo .local e executável do aplicativo está instalado. Se encontrado, o aplicativo usará esse arquivo de componente, independentemente de qualquer caminho de pesquisa de diretório definido no aplicativo ou no Registro. Se não for encontrado, o arquivo de componente no caminho de pesquisa definido será usado.

O utilitário de instalação deve fazer o seguinte para instalar o aplicativo com redirecionamento DLL/COM:

-   Um arquivo .local vazio deve ser copiado para a mesma pasta que o arquivo executável do aplicativo.
-   Todos os componentes, DLL e arquivos .ocx usados pelo aplicativo devem ser copiados para a mesma pasta que o arquivo executável do aplicativo.
-   Componentes COM isolados devem ser registrados com Windows para que diferentes versões do assembly não entre em conflito quando carregadas na memória ao mesmo tempo. O processo de registro requer que, embora a implementação do componente possa mudar entre versões, determinados metadados COM, como CLSID, ProgID, Biblioteca de Tipos e Modelo de Threading, não podem.
-   Se o aplicativo for instalado usando o Windows, o diretório do aplicativo poderá ser protegido usando a tabela LockPermissions. Normalmente, o sistema recebe acesso de leitura, gravação e execução; todos os outros processos só receberão acesso de execução e leitura.

 

 



