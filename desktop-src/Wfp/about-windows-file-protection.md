---
description: O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais que são instalados como parte do sistema operacional.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Sobre Proteção de Recursos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761086"
---
# <a name="about-windows-resource-protection"></a>Sobre Proteção de Recursos do Windows

O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais que são instalados como parte do sistema operacional. Ele se tornou disponível a partir do Windows Server 2008 e do Windows Vista. Permissão para acesso completo para modificar recursos protegidos por WRP é restrita a TrustedInstaller. Os recursos protegidos por WRP só podem ser alterados usando os [mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md) com o serviço instalador de módulos do Windows. A proteção desses recursos impede falhas de aplicativos e do sistema operacional.

Os aplicativos não devem tentar modificar os recursos protegidos por WRP porque eles são usados pelo Windows e por outros aplicativos. Se um aplicativo tentar modificar um recurso protegido por WRP, ele poderá ter os seguintes resultados.

-   Instaladores de aplicativos que tentam substituir, modificar ou excluir arquivos críticos do Windows ou chaves do registro podem falhar ao instalar o aplicativo e receberão uma mensagem de erro informando que o acesso ao recurso foi negado.
-   Os aplicativos que tentam adicionar ou remover subchaves ou alterar os valores das chaves de registro protegidas podem falhar e receberão uma mensagem de erro informando que o acesso ao recurso foi negado.
-   Os aplicativos que dependem de gravar qualquer informação em chaves, pastas ou arquivos protegidos do registro podem falhar.

WRP é o novo nome da WFP (proteção de arquivo do Windows). A WRP protege chaves e pastas do registro, bem como arquivos essenciais do sistema. A WFP estava disponível no Microsoft Windows Server 2003 e no Windows XP. A WRP substitui a WFP no Windows Server 2008 e no Windows Vista.

Os tópicos a seguir descrevem a WRP:

-   [Lista de recursos protegidos](protected-file-list.md)
-   [Detectando substituição de recursos](detecting-file-replacement.md)
-   [Mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md)
-   [Verificador de arquivos do sistema](system-file-checker.md)
-   [Considerações sobre administração remota](remote-administration-considerations.md)

 

 



