---
title: Os arquivos de cabeçalho
description: O arquivo de cabeçalho da interface (Name. h) contém definições de tipo e declarações de função com base na definição de interface no arquivo IDL atual, bem como todos os tipos de dados e operações declarados nos arquivos incluídos na diretiva \ include.
ms.assetid: 81fac1fa-6bd7-4a3e-8aa6-5104d4b25b55
keywords:
- arquivos de cabeçalho MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ae80877b88d8061769b0d6bd56c13469427fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105787510"
---
# <a name="the-header-files"></a>Os arquivos de cabeçalho

O arquivo de cabeçalho de interface (Name. h) contém definições de tipo e declarações de função com base na definição de interface no arquivo IDL atual, bem como todos os tipos de dados e operações declarados nos arquivos incluídos com a \# diretiva include. Os tipos de dados dos arquivos importados com a diretiva de importação não são replicados para o arquivo de cabeçalho; em vez disso, o arquivo de cabeçalho gerado contém uma linha de inclusão para o arquivo H gerado a partir do arquivo importado.

Inclua esse arquivo nos arquivos de origem para a DLL de proxy e para aplicativos cliente que usam a interface.

O nome padrão de um arquivo de cabeçalho gerado a partir de um file. idl é File. h. A opção de compilador [**/header**](-header.md) MIDL substitui o nome padrão do arquivo de cabeçalho da interface.

 

 




