---
title: O arquivo de cabeçalho
description: O arquivo de cabeçalho contém definições de todos os tipos de dados e operações declarados no arquivo IDL, bem como todos os tipos de dados e operações declarados nos arquivos incluídos na diretiva \ include.
ms.assetid: 51789b42-e01c-4233-97da-5e0a044f596f
keywords:
- MIDL e PRC de MIDL, interfaces, arquivo de cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61331d8bb72d322987c13d02b04632c95424e755
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005853"
---
# <a name="the-header-file"></a><span data-ttu-id="bffcb-104">O arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bffcb-104">The Header File</span></span>

<span data-ttu-id="bffcb-105">O arquivo de cabeçalho contém definições de todos os tipos de dados e operações declarados no arquivo IDL, bem como todos os tipos de dados e operações declarados nos arquivos incluídos na \# diretiva include.</span><span class="sxs-lookup"><span data-stu-id="bffcb-105">The header file contains definitions of all data types and operations declared in the IDL file, as well as all data types and operations declared in the files included with the \#include directive.</span></span> <span data-ttu-id="bffcb-106">Os tipos de dados dos arquivos importados com a diretiva de importação não são replicados para o arquivo de cabeçalho; em vez disso, o arquivo de cabeçalho gerado contém uma linha de inclusão para o arquivo H gerado a partir do arquivo importado.</span><span class="sxs-lookup"><span data-stu-id="bffcb-106">Data types from the files imported with the import directive are not replicated to the header file; instead the generated header file contains an include line to the H file generated from the imported file.</span></span> <span data-ttu-id="bffcb-107">O arquivo de cabeçalho deve ser incluído por todos os módulos de aplicativo que chamam as operações definidas, implementar as operações definidas ou manipular os tipos definidos.</span><span class="sxs-lookup"><span data-stu-id="bffcb-107">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="bffcb-108">O compilador MIDL alterna [**/header**](-header.md) e [**/out**](-out.md) afeta o arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="bffcb-108">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




