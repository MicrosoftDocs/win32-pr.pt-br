---
description: Os autores de pacotes de instalação podem especificar que o instalador Copie os arquivos compartilhados (normalmente DLLs compartilhadas) de um aplicativo para a pasta desse aplicativo em vez de um local compartilhado.
ms.assetid: eb5f7088-30e0-4644-813a-c93e6f56ccbf
title: Componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08095e72862a94474b7096950ac5ed3b331e806456e72982ee9d7374ab9511b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013174"
---
# <a name="isolated-components"></a>Componentes isolados

Os autores de pacotes de instalação podem especificar que o instalador Copie os arquivos compartilhados (normalmente DLLs compartilhadas) de um aplicativo para a pasta desse aplicativo em vez de um local compartilhado. Esse conjunto particular de arquivos (DLLs) é usado somente pelo aplicativo. Isolar o aplicativo junto com seus componentes compartilhados dessa maneira tem as seguintes vantagens:

-   O aplicativo sempre usa as versões dos arquivos compartilhados com as quais ele foi implantado.
-   A instalação do aplicativo não substitui outras versões dos arquivos compartilhados por outros aplicativos.
-   As instalações subsequentes de outros aplicativos que usam versões diferentes dos arquivos compartilhados não podem substituir os arquivos usados por esse aplicativo.

Como a implementação atual do COM mantém um único caminho completo no registro para cada par de CLSID/contexto, ele força todos os aplicativos a usarem a mesma versão de uma DLL compartilhada. para permitir que um aplicativo mantenha uma cópia privada de um servidor COM, o carregador do sistema no Windows 2000 verifica a presença de um. Arquivo LOCAL na pasta do aplicativo. Se o carregador do sistema detectar um. Arquivo LOCAL, ele altera sua lógica de pesquisa para preferir DLLs localizadas na mesma pasta que o aplicativo.

quando Windows Installer executa a [ação IsolateComponents](isolatecomponents-action.md) , eles copiam os arquivos do componente (normalmente uma DLL compartilhada) especificada na \_ coluna compartilhada do componente da [tabela IsolatedComponent](isolatedcomponent-table.md) na mesma pasta que o componente (normalmente um arquivo de .exe) especificado na \_ coluna aplicativo do componente. O instalador cria um arquivo nesse diretório, com zero bytes de comprimento, tendo o nome de arquivo curto do arquivo de chave para o aplicativo de componente \_ (normalmente, o nome é o mesmo que o .exe do aplicativo) acrescentado com. LOCAL. O instalador usa o registro para o componente em seu local compartilhado e não grava nenhuma informação de registro para a cópia do componente no local privado.

Para obter mais informações, consulte:

-   [Instalação de componentes isolados](installation-of-isolated-components.md)
-   [Reinstalação de componentes isolados](reinstallation-of-isolated-components.md)
-   [Remoção de componentes isolados](removal-of-isolated-components.md)
-   [Usando componentes isolados](using-isolated-components.md)

 

 



