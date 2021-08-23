---
title: O arquivo de header
description: O arquivo de header contém definições de todos os tipos de dados e operações declaradas no arquivo IDL, bem como todos os tipos de dados e operações declarados nos arquivos incluídos com a diretiva \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL e RPC MIDL, interfaces, arquivo de header
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd107bbf741f3259ac474d03a3ec1eba5c4ab8217df3ff6afa5ef45e7b4945a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582126"
---
# <a name="the-header-file"></a>O arquivo de header

O arquivo de header contém definições de todos os tipos de dados e operações declarados no arquivo IDL, bem como todos os tipos de dados e operações declarados nos arquivos incluídos com a diretiva \# include. Os tipos de dados dos arquivos importados com a diretiva import não são replicados para o arquivo de header; em vez disso, o arquivo de header gerado contém uma linha de inclusão para o arquivo H gerado do arquivo importado. O arquivo de header deve ser incluído por todos os módulos de aplicativo que chamam as operações definidas, implementam as operações definidas ou manipulam os tipos definidos.

As opções [**/header**](-header.md) e [**/out**](-out.md) do compilador MIDL afetam o arquivo de header.

 

 




