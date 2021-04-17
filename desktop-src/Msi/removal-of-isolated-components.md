---
description: Windows Installer executa as seguintes ações durante a remoção de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Remoção de componentes isolados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751423"
---
# <a name="removal-of-isolated-components"></a>Remoção de componentes isolados

Windows Installer executa as seguintes ações durante a remoção de um aplicativo quando o pacote contém componentes isolados. Normalmente, \_ o componente compartilhado é uma DLL que é compartilhada por \_ aplicativo de componente e outros executáveis do cliente.

## <a name="uninstall"></a>Desinstalar

-   Remova os arquivos do componente \_ compartilhado da pasta que contém o \_ aplicativo de componente somente se o aplicativo de componente \_ também estiver sendo removido.
-   Se o bit msidbComponentAttributesSharedDllRefCount for definido na [tabela de componentes](component-table.md) , reduza o Refcount SharedDLL.
-   Remova o. Arquivo de byte zero LOCAL da pasta que contém o \_ aplicativo de componente.
-   Remover aplicativo de componente \_ da lista de clientes do componente \_ compartilhado.
-   Remova todos os recursos do aplicativo de componente \_ como de costume.

Se houver outros produtos restantes na lista de clientes do componente \_ compartilhado:

-   Não remova nenhum arquivo do local compartilhado do componente \_ compartilhado.

Se o Refcount SharedDLL para o componente \_ compartilhado for 0 depois de ser decrementado, ou se não houver outros clientes restantes do componente \_ compartilhado:

-   Remova os arquivos do componente \_ compartilhado do local compartilhado.
-   Processar todas as ações de desinstalação com relação a esse componente.

 

 



