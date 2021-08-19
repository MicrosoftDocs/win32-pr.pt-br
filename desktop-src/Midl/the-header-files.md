---
title: Os arquivos de header
description: O arquivo de header da interface (Name.h) contém definições de tipo e declarações de função com base na definição da interface no arquivo IDL atual, bem como todos os tipos de dados e operações declarados nos arquivos incluídos com a diretiva \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- arquivos de header MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac9bc5e8b5edd091450af670fd51d251326029f13e1f88a6d5a9116faa5b4447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013514"
---
# <a name="the-header-files"></a>Os arquivos de header

O arquivo de header da interface (Name.h) contém definições de tipo e declarações de função com base na definição da interface no arquivo IDL atual, bem como todos os tipos de dados e operações declarados nos arquivos incluídos com a diretiva \# include. Os tipos de dados dos arquivos importados com a diretiva import não são replicados para o arquivo de header; em vez disso, o arquivo de header gerado contém uma linha de inclusão para o arquivo H gerado do arquivo importado.

Inclua esse arquivo nos arquivos de origem para a DLL de proxy e para aplicativos cliente que usam a interface .

O nome padrão para um arquivo de header gerado de um file.idl é File.h. A [**opção do compilador /header**](-header.md) MIDL substitui o nome padrão do arquivo de header da interface.

 

 




