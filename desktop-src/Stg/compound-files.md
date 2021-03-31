---
title: arquivos compostos
description: Embora você possa implementar seus próprios objetos e interfaces de armazenamento estruturado, o COM fornece uma implementação padrão chamada arquivos compostos.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159428"
---
# <a name="compound-files"></a>arquivos compostos

Embora você possa implementar seus próprios objetos e interfaces de armazenamento estruturado, o COM fornece uma implementação padrão chamada arquivos compostos. O uso de arquivos compostos poupa o trabalho de codificar sua própria implementação de armazenamento estruturado e confere vários benefícios adicionais derivados de aderir a um padrão definido. Esses benefícios incluem o seguinte:

-   **Independência de plataforma e sistema de arquivos**. Como a implementação dos arquivos compostos do COM é executada na parte superior dos sistemas de arquivos simples existentes, os arquivos compostos armazenados no sistema de arquivos FAT, no sistema de arquivos NTFS ou nos sistemas de arquivos do Macintosh podem ser abertos por aplicativos que usam qualquer um dos outros sistemas de arquivos.
-   **Pesquisável**. Como os objetos separados em um arquivo composto são salvos em um formato padrão e podem ser acessados usando interfaces COM e APIs padrão, qualquer utilitário de navegador usando essas interfaces e APIs pode listar os objetos no arquivo, mesmo que os dados dentro de um determinado objeto possam estar em um formato proprietário.
-   **Acesso a determinados dados internos**. Como a implementação dos arquivos compostos fornece maneiras padrão de gravar determinados tipos de dados — informações de resumo, por exemplo — os aplicativos podem ler esses dados usando interfaces e APIs COM.

 

 




