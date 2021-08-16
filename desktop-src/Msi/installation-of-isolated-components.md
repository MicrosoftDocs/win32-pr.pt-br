---
description: Windows O instalador executa as seguintes ações durante a instalação de um aplicativo quando o pacote contém componentes isolados. Normalmente, o Componente Compartilhado é uma DLL compartilhada pelo Aplicativo de Componente \_ e outros \_ executáveis do cliente.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Instalação de componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f842f626775dce436abedace96549fd55079c577885aad81492df861cd1a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634121"
---
# <a name="installation-of-isolated-components"></a>Instalação de componentes isolados

Windows O instalador executa as seguintes ações durante a instalação de um aplicativo quando o pacote contém componentes isolados. Normalmente, o Componente Compartilhado é uma DLL compartilhada pelo Aplicativo de Componente \_ e outros \_ executáveis do cliente.

## <a name="installation"></a>Instalação

-   Copie os arquivos do Componente Compartilhado na mesma pasta que o Aplicativo de Componente somente se o Aplicativo de Componente \_ também estiver sendo \_ \_ instalado.
-   Crie um arquivo de zero byte com o nome de arquivo curto do arquivo de chave do Aplicativo de \_ Componente. Localize esse arquivo na mesma pasta que o Aplicativo \_ de Componente. Anexar a extensão . LOCAL para esse nome de arquivo.
-   Incremente a refcount sharedDLL se o bit msidbComponentAttributesSharedDllRefCount for definido na coluna Atributos da [tabela Component](component-table.md).
-   Registre Aplicativo de Componente como um cliente do Componente Compartilhado e registre um caminho de chave apontando para \_ o local compartilhado do Componente \_ \_ Compartilhado.
-   Instale todos os recursos do Aplicativo de \_ Componente como de costume.

Se o Componente Compartilhado ou seu arquivo de chave já estiver instalado no computador, não copie os arquivos para o local \_ compartilhado do Componente \_ Compartilhado.

Se o Componente Compartilhado ou seu arquivo de chave \_ ainda não estiver instalado no computador:

-   Copie os arquivos do Componente \_ Compartilhado para o local compartilhado.
-   Processe todas as ações de instalação do Componente \_ Compartilhado.
-   Se Component Shared for um componente COM, registre o caminho COM completo de forma que a sintaxe \_ \[ $Component e \] \[ \# FileKey apontem \] \_ para o local compartilhado do Componente Compartilhado.

 

 



