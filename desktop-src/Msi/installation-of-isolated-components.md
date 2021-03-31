---
description: Windows Installer executa as seguintes ações durante a instalação de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: Instalação de componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647716"
---
# <a name="installation-of-isolated-components"></a>Instalação de componentes isolados

Windows Installer executa as seguintes ações durante a instalação de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.

## <a name="installation"></a>Instalação

-   Copie os arquivos do componente \_ compartilhado para a mesma pasta que o \_ aplicativo de componente somente se o aplicativo de componente \_ também estiver sendo instalado.
-   Crie um arquivo de byte zero com o nome de arquivo curto do arquivo de chave do \_ aplicativo de componente. Localize esse arquivo na mesma pasta que o aplicativo de componente \_ . Acrescente a extensão. LOCAL para esse nome de arquivo.
-   Aumente o Refcount SharedDLL se o bit msidbComponentAttributesSharedDllRefCount estiver definido na coluna atributos da tabela de [componentes](component-table.md).
-   Registre o \_ aplicativo componente como um cliente do componente \_ compartilhado e registre um caminho de chave apontando para o local compartilhado do componente \_ compartilhado.
-   Instale todos os recursos do aplicativo de componente \_ como de costume.

Se o componente \_ compartilhado ou seu arquivo de chave já estiver instalado no computador, não copie os arquivos para o local compartilhado do componente \_ compartilhado.

Se \_ o componente compartilhado ou seu arquivo de chave ainda não estiver instalado no computador:

-   Copie os arquivos do componente \_ compartilhado para o local compartilhado.
-   Processar todas as ações de instalação para componente \_ compartilhado.
-   Se o componente \_ compartilhado for um componente com, registre o caminho com completo, de modo que a sintaxe \[ $Component \] e \[ \# FileKey \] apontem para o local compartilhado do componente \_ compartilhado.

 

 



