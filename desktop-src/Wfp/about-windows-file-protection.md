---
description: Windows A WRP (proteção de recurso) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais que são instalados como parte do sistema operacional.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: sobre Proteção de Recursos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d06110c668e48a401cc329d79982e7c1b2746408ce45da9b7b3dffaca40b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134190"
---
# <a name="about-windows-resource-protection"></a>sobre Proteção de Recursos do Windows

Windows A WRP (proteção de recurso) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais que são instalados como parte do sistema operacional. ele se tornou disponível a partir do Windows Server 2008 e Windows Vista. Permissão para acesso completo para modificar recursos protegidos por WRP é restrita a TrustedInstaller. os recursos protegidos por WRP só podem ser alterados usando os [mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md) com o serviço instalador de módulos Windows. A proteção desses recursos impede falhas de aplicativos e do sistema operacional.

os aplicativos não devem tentar modificar os recursos protegidos por WRP porque eles são usados por Windows e outros aplicativos. Se um aplicativo tentar modificar um recurso protegido por WRP, ele poderá ter os seguintes resultados.

-   instaladores de aplicativos que tentam substituir, modificar ou excluir arquivos críticos Windows ou chaves do registro podem falhar ao instalar o aplicativo e receberão uma mensagem de erro informando que o acesso ao recurso foi negado.
-   Os aplicativos que tentam adicionar ou remover subchaves ou alterar os valores das chaves de registro protegidas podem falhar e receberão uma mensagem de erro informando que o acesso ao recurso foi negado.
-   Os aplicativos que dependem de gravar qualquer informação em chaves, pastas ou arquivos protegidos do registro podem falhar.

WRP é o novo nome para a proteção de arquivo Windows (WFP). A WRP protege chaves e pastas do registro, bem como arquivos essenciais do sistema. a WFP estava disponível no Microsoft Windows Server 2003 e no Windows XP. a WRP substitui a WFP no Windows Server 2008 e Windows Vista.

Os tópicos a seguir descrevem a WRP:

-   [Lista de recursos protegidos](protected-file-list.md)
-   [Detectando substituição de recursos](detecting-file-replacement.md)
-   [Mecanismos de substituição de recursos com suporte](supported-file-replacement-mechanisms.md)
-   [ Verificador de Arquivos do Sistema](system-file-checker.md)
-   [Considerações sobre administração remota](remote-administration-considerations.md)

 

 



