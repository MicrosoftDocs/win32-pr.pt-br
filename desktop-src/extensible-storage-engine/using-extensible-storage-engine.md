---
description: 'Saiba mais sobre: usando o mecanismo de armazenamento extensível'
title: Usando o mecanismo de armazenamento extensível
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 636c3fa96692b8c48f9a175b5fa7d34c53314e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791332"
---
# <a name="using-extensible-storage-engine"></a><span data-ttu-id="2840c-103">Usando o mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="2840c-103">Using Extensible Storage Engine</span></span>


<span data-ttu-id="2840c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2840c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="using-extensible-storage-engine"></a><span data-ttu-id="2840c-105">Usando o mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="2840c-105">Using Extensible Storage Engine</span></span>

<span data-ttu-id="2840c-106">Esta seção contém informações gerais sobre como usar as seguintes partes da API do ESE.</span><span class="sxs-lookup"><span data-stu-id="2840c-106">This section contains general information about how to use the following parts of the ESE API.</span></span>

  - [<span data-ttu-id="2840c-107">Colunas</span><span class="sxs-lookup"><span data-stu-id="2840c-107">Columns</span></span>](./columns.md)

  - [<span data-ttu-id="2840c-108">Indexação na tabela</span><span class="sxs-lookup"><span data-stu-id="2840c-108">Indexing in the Table</span></span>](./indexing-in-the-table.md)

  - [<span data-ttu-id="2840c-109">Criando bancos de dados</span><span class="sxs-lookup"><span data-stu-id="2840c-109">Creating Databases</span></span>](./creating-databases.md)

  - [<span data-ttu-id="2840c-110">Transações</span><span class="sxs-lookup"><span data-stu-id="2840c-110">Transactions</span></span>](./transactions.md)

  - [<span data-ttu-id="2840c-111">Erros do ESE</span><span class="sxs-lookup"><span data-stu-id="2840c-111">ESE Errors</span></span>](./extensible-storage-engine-errors.md)

  - [<span data-ttu-id="2840c-112">Arquivos ESE</span><span class="sxs-lookup"><span data-stu-id="2840c-112">ESE Files</span></span>](./extensible-storage-engine-files.md)

<span data-ttu-id="2840c-113">Os arquivos de origem do programa devem incluir o arquivo de cabeçalho ESENT. h para acessar protótipos de função e definições de estrutura para a API do mecanismo de armazenamento extensível.</span><span class="sxs-lookup"><span data-stu-id="2840c-113">Your program source files should include the esent.h header file to access function prototypes and structure definitions for the Extensible Storage Engine API.</span></span> <span data-ttu-id="2840c-114">Os desenvolvedores podem usar o arquivo de biblioteca ESENT. lib para criar aplicativos que usam a API do mecanismo de armazenamento extensível.</span><span class="sxs-lookup"><span data-stu-id="2840c-114">Developers can use the esent.lib library file to build applications that use the Extensible Storage Engine API.</span></span> <span data-ttu-id="2840c-115">Em tempo de execução, os aplicativos são vinculados ao esent.dll.</span><span class="sxs-lookup"><span data-stu-id="2840c-115">At runtime, applications link to the esent.dll.</span></span>
