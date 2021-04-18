---
description: A ação RemoveODBC remove as fontes de dados, os tradutores e os drivers listados para remoção durante a instalação.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Ação RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787496"
---
# <a name="removeodbc-action"></a><span data-ttu-id="960b2-103">Ação RemoveODBC</span><span class="sxs-lookup"><span data-stu-id="960b2-103">RemoveODBC Action</span></span>

<span data-ttu-id="960b2-104">A ação RemoveODBC remove as fontes de dados, os tradutores e os drivers listados para remoção durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="960b2-104">The RemoveODBC action removes the data sources, translators, and drivers listed for removal during the installation.</span></span> <span data-ttu-id="960b2-105">Essa ação consulta a tabela [ODBCDataSource](odbcdatasource-table.md), a [tabela ODBCTranslator](odbctranslator-table.md)e a [tabela ODBCDriver](odbcdriver-table.md) para cada fonte de dados, Tradutor ou driver agendado para remoção.</span><span class="sxs-lookup"><span data-stu-id="960b2-105">This action queries the [ODBCDataSource table](odbcdatasource-table.md), [ODBCTranslator table](odbctranslator-table.md), and [ODBCDriver table](odbcdriver-table.md) for each data source, translator, or driver scheduled for removal.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="960b2-106">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="960b2-106">Sequence Restrictions</span></span>

<span data-ttu-id="960b2-107">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="960b2-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="960b2-108">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="960b2-108">ActionData Messages</span></span>

<span data-ttu-id="960b2-109">Para cada driver instalado.</span><span class="sxs-lookup"><span data-stu-id="960b2-109">For each driver installed.</span></span>



| <span data-ttu-id="960b2-110">Campo</span><span class="sxs-lookup"><span data-stu-id="960b2-110">Field</span></span> | <span data-ttu-id="960b2-111">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="960b2-111">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="960b2-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="960b2-112">\[1\]</span></span> | <span data-ttu-id="960b2-113">Descrição do driver.</span><span class="sxs-lookup"><span data-stu-id="960b2-113">Driver description.</span></span> <span data-ttu-id="960b2-114">A chave do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="960b2-114">The ODBC driver key.</span></span> |
| <span data-ttu-id="960b2-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="960b2-115">\[2\]</span></span> | <span data-ttu-id="960b2-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="960b2-116">ComponentId</span></span>                              |



 

<span data-ttu-id="960b2-117">Para cada tradutor instalado.</span><span class="sxs-lookup"><span data-stu-id="960b2-117">For each translator installed.</span></span>



| <span data-ttu-id="960b2-118">Campo</span><span class="sxs-lookup"><span data-stu-id="960b2-118">Field</span></span> | <span data-ttu-id="960b2-119">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="960b2-119">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="960b2-120">\[1\]</span><span class="sxs-lookup"><span data-stu-id="960b2-120">\[1\]</span></span> | <span data-ttu-id="960b2-121">Descrição do driver.</span><span class="sxs-lookup"><span data-stu-id="960b2-121">Driver description.</span></span> <span data-ttu-id="960b2-122">A chave do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="960b2-122">The ODBC driver key.</span></span> |
| <span data-ttu-id="960b2-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="960b2-123">\[2\]</span></span> | <span data-ttu-id="960b2-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="960b2-124">ComponentId</span></span>                              |



 

<span data-ttu-id="960b2-125">Para cada fonte de dados instalada.</span><span class="sxs-lookup"><span data-stu-id="960b2-125">For each data source installed.</span></span>



| <span data-ttu-id="960b2-126">Campo</span><span class="sxs-lookup"><span data-stu-id="960b2-126">Field</span></span> | <span data-ttu-id="960b2-127">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="960b2-127">Description of action data</span></span>                              |
|-------|---------------------------------------------------------|
| <span data-ttu-id="960b2-128">\[1\]</span><span class="sxs-lookup"><span data-stu-id="960b2-128">\[1\]</span></span> | <span data-ttu-id="960b2-129">Descrição do driver.</span><span class="sxs-lookup"><span data-stu-id="960b2-129">Driver description.</span></span> <span data-ttu-id="960b2-130">A chave do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="960b2-130">The ODBC driver key.</span></span>                |
| <span data-ttu-id="960b2-131">\[2\]</span><span class="sxs-lookup"><span data-stu-id="960b2-131">\[2\]</span></span> | <span data-ttu-id="960b2-132">ComponentId</span><span class="sxs-lookup"><span data-stu-id="960b2-132">ComponentId</span></span>                                             |
| <span data-ttu-id="960b2-133">\[3\]</span><span class="sxs-lookup"><span data-stu-id="960b2-133">\[3\]</span></span> | <span data-ttu-id="960b2-134">Registro: SQL \_ Remove \_ DSN ou SQL \_ Remove \_ Sys \_ DSN</span><span class="sxs-lookup"><span data-stu-id="960b2-134">Registration: SQL\_REMOVE\_DSN or SQL\_REMOVE\_SYS\_DSN</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="960b2-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="960b2-135">Remarks</span></span>

<span data-ttu-id="960b2-136">Se a contagem de uso do ODBC e a contagem de uso do arquivo se tornarem zero, o arquivo será removido.</span><span class="sxs-lookup"><span data-stu-id="960b2-136">If both the ODBC usage count and the file usage count become zero, the file is removed.</span></span> <span data-ttu-id="960b2-137">O registro depende de contagens de uso de ODBC e a remoção de arquivo é baseada em contagens de referência de chave de DLLs compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="960b2-137">Registration is dependent on ODBC usage counts and file removal is based on shared DLLs key reference counts.</span></span>

 

 



