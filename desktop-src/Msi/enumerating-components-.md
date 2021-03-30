---
description: Windows Installer 5,0 em execução no Windows Server 2008 R2 ou no Windows 7 podem enumerar todos os componentes instalados no computador e obter o caminho da chave para o componente.
ms.assetid: a6676340-1695-48c7-a1e4-7a02a7bc3fef
title: Enumerando componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea314ee91c35fb021f5a8da64b6430e8cf950ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661861"
---
# <a name="enumerating-components"></a>Enumerando componentes

Windows Installer 5,0 em execução no Windows Server 2008 R2 ou no Windows 7 podem enumerar todos os componentes instalados no computador e obter o caminho da chave para o componente. Um pacote criado para o Windows Installer 5,0 pode usar as funções [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa), [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)e [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) para Pesquisar componentes e produtos em contas de usuário e contextos de instalação. As funções [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa), [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)e [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) retornam apenas informações para componentes e produtos instalados para a conta de usuário que chamou a função. Várias chamadas para essas funções, pelo menos uma vez para cada conta de usuário, são necessárias para coletar informações de todo o computador.

A função [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa) enumera os componentes instalados. A função recupera um código de componente cada vez que ele é chamado. O [**objeto de componente**](components.md) recebe informações sobre um componente instalado por essa função.

A função [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa) enumera os produtos que são clientes de um componente instalado especificado. O [**objeto cliente**](client.md) recebe informações sobre um cliente por essa função.

A função [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa) retorna o caminho completo para um componente instalado. A função retornará a chave do registro se o caminho da chave do componente for uma chave do registro. O [**objeto ComponentInfo**](componentinfo.md) recebe informações sobre um componente instalado por essa função.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Essa funcionalidade está disponível a partir do Windows Installer 5,0 em execução no Windows 7 ou no Windows Server 2008 R2.

 

 



