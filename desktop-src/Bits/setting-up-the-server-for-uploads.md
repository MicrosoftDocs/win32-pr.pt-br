---
title: Configurando o servidor para carregamentos
description: Para carregar arquivos em um servidor usando BITS, o servidor deve ter o IIS e a extensão de servidor do BITS ISAPI instalados. Para os requisitos do IIS, consulte requisitos do IIS para carregamentos do BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159353"
---
# <a name="setting-up-the-server-for-uploads"></a>Configurando o servidor para carregamentos

Para carregar arquivos em um servidor usando BITS, o servidor deve ter o IIS e a extensão de servidor do BITS ISAPI instalados. Para os requisitos do IIS, consulte [requisitos do IIS para carregamentos do bits](iis-requirements-for-bits-uploads.md).

Para obter informações sobre como configurar o diretório virtual do IIS que o BITS usa para carregamentos, consulte os tópicos a seguir.

-   [Definindo permissões em diretórios virtuais](setting-permissions-on-virtual-directories.md)
-   [Gravando um script para configurar o diretório virtual](writing-a-script-to-configure-the-virtual-directory.md)
-   [Usando a interface do usuário do IIS para configurar o diretório virtual](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Impedindo vários carregamentos](preventing-multiple-uploads.md)
-   [Práticas recomendadas de upload](upload-best-practices.md)

> [!Note]  
> Algumas instalações do IIS incluem o componente de filtragem do UrlScan. Se o UrlScan estiver habilitado, o administrador deverá adicionar o verbo "post do BITS \_ " à lista de VERBOS http permitidos do URLScan. Caso contrário, haverá falha nos carregamentos do cliente BITS. Para obter mais detalhes sobre como habilitar verbos no UrlScan, consulte a documentação do UrlScan.

 

 

 




