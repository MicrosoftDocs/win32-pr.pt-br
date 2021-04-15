---
description: 'Saiba mais sobre: parâmetros do sistema do mecanismo de armazenamento extensível'
title: Parâmetros do sistema do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502301"
---
# <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="31ae2-103">Parâmetros do sistema do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="31ae2-103">Extensible Storage Engine System Parameters</span></span>


<span data-ttu-id="31ae2-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="31ae2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="31ae2-105">Parâmetros do sistema do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="31ae2-105">Extensible Storage Engine System Parameters</span></span>

<span data-ttu-id="31ae2-106">As constantes a seguir são usadas como valores para o parâmetro *paramid* das funções [JetGetSystemParameter](./jetgetsystemparameter-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="31ae2-106">The following constants are used as values for the *paramid* parameter of the [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) functions.</span></span>

  - [<span data-ttu-id="31ae2-107">Parâmetros de backup e restauração</span><span class="sxs-lookup"><span data-stu-id="31ae2-107">Backup and Restore Parameters</span></span>](./backup-and-restore-parameters.md)

  - [<span data-ttu-id="31ae2-108">Parâmetros de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="31ae2-108">Callback Parameters</span></span>](./callback-parameters.md)

  - [<span data-ttu-id="31ae2-109">Parâmetros de Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="31ae2-109">Database Parameters</span></span>](./database-parameters.md)

  - [<span data-ttu-id="31ae2-110">Parâmetros de cache do banco de dados</span><span class="sxs-lookup"><span data-stu-id="31ae2-110">Database Cache Parameters</span></span>](./database-cache-parameters.md)

  - [<span data-ttu-id="31ae2-111">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="31ae2-111">Error Handling Parameters</span></span>](./error-handling-parameters.md)

  - [<span data-ttu-id="31ae2-112">Parâmetros do log de eventos</span><span class="sxs-lookup"><span data-stu-id="31ae2-112">Event Log Parameters</span></span>](./event-log-parameters.md)

  - [<span data-ttu-id="31ae2-113">Parâmetros de e/s</span><span class="sxs-lookup"><span data-stu-id="31ae2-113">I/O Parameters</span></span>](./i-o-parameters.md)

  - [<span data-ttu-id="31ae2-114">Parâmetros de Índice</span><span class="sxs-lookup"><span data-stu-id="31ae2-114">Index Parameters</span></span>](./index-parameters.md)

  - [<span data-ttu-id="31ae2-115">Parâmetros informativos</span><span class="sxs-lookup"><span data-stu-id="31ae2-115">Informational Parameters</span></span>](./informational-parameters.md)

  - [<span data-ttu-id="31ae2-116">Parâmetros meta</span><span class="sxs-lookup"><span data-stu-id="31ae2-116">Meta Parameters</span></span>](./meta-parameters.md)

  - [<span data-ttu-id="31ae2-117">Parâmetros do recurso</span><span class="sxs-lookup"><span data-stu-id="31ae2-117">Resource Parameters</span></span>](./resource-parameters.md)

  - [<span data-ttu-id="31ae2-118">Parâmetros de banco de dados temporários</span><span class="sxs-lookup"><span data-stu-id="31ae2-118">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

  - [<span data-ttu-id="31ae2-119">Parâmetros de Log de Transação</span><span class="sxs-lookup"><span data-stu-id="31ae2-119">Transaction Log Parameters</span></span>](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a><span data-ttu-id="31ae2-120">Formato de descrição do parâmetro do sistema</span><span class="sxs-lookup"><span data-stu-id="31ae2-120">System Parameter Description Format</span></span>

<span data-ttu-id="31ae2-121">Cada parâmetro do sistema será descrito usando o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="31ae2-121">Each system parameter will be described using the following format:</span></span>

<span data-ttu-id="31ae2-122">JET_paramX</span><span class="sxs-lookup"><span data-stu-id="31ae2-122">JET_paramX</span></span>

<span data-ttu-id="31ae2-123">Descrição do parâmetro do sistema JET_paramX.</span><span class="sxs-lookup"><span data-stu-id="31ae2-123">Description of the JET_paramX system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31ae2-124">Valor padrão:</span><span class="sxs-lookup"><span data-stu-id="31ae2-124">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-125">O valor padrão do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="31ae2-125">The default value of the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31ae2-126">Tipo:</span><span class="sxs-lookup"><span data-stu-id="31ae2-126">Type:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-127">O tipo de dados do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="31ae2-127">The data type of the parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31ae2-128">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="31ae2-128">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-129">Os valores válidos para o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="31ae2-129">The legal values for the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31ae2-130">Escopo:</span><span class="sxs-lookup"><span data-stu-id="31ae2-130">Scope:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-131">O parâmetro é global ou por instância?</span><span class="sxs-lookup"><span data-stu-id="31ae2-131">Is the parameter Global or per Instance?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31ae2-132">Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="31ae2-132">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-133">O parâmetro pode ser definido se existir alguma instância?</span><span class="sxs-lookup"><span data-stu-id="31ae2-133">Can the parameter be set if any instances exist?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31ae2-134">Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="31ae2-134">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-135">O parâmetro pode ser definido quando inicializado?</span><span class="sxs-lookup"><span data-stu-id="31ae2-135">Can the parameter be set when initialized?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31ae2-136">Afeta o layout físico:</span><span class="sxs-lookup"><span data-stu-id="31ae2-136">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-137">O parâmetro afeta os arquivos em disco?</span><span class="sxs-lookup"><span data-stu-id="31ae2-137">Does the parameter affect the files on disk?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31ae2-138">Afeta a confiabilidade:</span><span class="sxs-lookup"><span data-stu-id="31ae2-138">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-139">O parâmetro afeta a confiabilidade do mecanismo?</span><span class="sxs-lookup"><span data-stu-id="31ae2-139">Does the parameter affect engine reliability?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31ae2-140">Afeta o desempenho:</span><span class="sxs-lookup"><span data-stu-id="31ae2-140">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-141">O parâmetro afeta o desempenho do mecanismo?</span><span class="sxs-lookup"><span data-stu-id="31ae2-141">Does the parameter affect engine performance?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31ae2-142">Afeta os recursos:</span><span class="sxs-lookup"><span data-stu-id="31ae2-142">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-143">O parâmetro afeta os recursos do mecanismo?</span><span class="sxs-lookup"><span data-stu-id="31ae2-143">Does the parameter affect engine resources?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31ae2-144">Disponibilidade:</span><span class="sxs-lookup"><span data-stu-id="31ae2-144">Availability:</span></span></p></td>
<td><p><span data-ttu-id="31ae2-145">Versões do Windows que dão suporte ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="31ae2-145">Releases of Windows that support the parameter.</span></span></p></td>
</tr>
</tbody>
</table>
