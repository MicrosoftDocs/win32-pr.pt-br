---
title: Configurando o servidor para uploads
description: Para carregar arquivos em um servidor usando BITS, o servidor deve ter o IIS e o ISAPI de extensão do servidor BITS instalados. Para requisitos do IIS, consulte Requisitos do IIS para uploads de BITS.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e075478f6e0335c6bf601a9289d93d4d3fac2aefd9e4f1ef820e938a1bfc0ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004716"
---
# <a name="setting-up-the-server-for-uploads"></a>Configurando o servidor para uploads

Para carregar arquivos em um servidor usando BITS, o servidor deve ter o IIS e o ISAPI de extensão do servidor BITS instalados. Para requisitos do IIS, consulte [Requisitos do IIS para uploads de BITS.](iis-requirements-for-bits-uploads.md)

Para obter informações sobre como configurar o diretório virtual do IIS que o BITS usa para uploads, consulte os tópicos a seguir.

-   [Definindo permissões em diretórios virtuais](setting-permissions-on-virtual-directories.md)
-   [Escrevendo um script para configurar o diretório virtual](writing-a-script-to-configure-the-virtual-directory.md)
-   [Usando a interface do usuário do IIS para configurar o diretório virtual](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [Impedindo vários uploads](preventing-multiple-uploads.md)
-   [Upload Práticas recomendadas](upload-best-practices.md)

> [!Note]  
> Algumas instalações do IIS incluem o componente de filtragem UrlScan. Se UrlScan estiver habilitado, o administrador deverá adicionar o verbo "BITS POST" à lista de \_ verbos HTTP permitidos do UrlScan. Caso contrário, os uploads do cliente BITS falharão. Para obter mais detalhes sobre a habilitação de verbos no UrlScan, consulte a documentação do UrlScan.

 

 

 




