---
description: Antes de usar um log de arquivos, você deve chamar SetupInitializeFileLog para abri-lo ou criá-lo. Ao chamar essa função, você pode especificar sinalizadores para criar ou substituir um log de arquivo, abrir o log do sistema ou abrir um log de arquivo como somente leitura.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Usando o log de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922979"
---
# <a name="using-the-file-log"></a><span data-ttu-id="9388e-104">Usando o log de arquivos</span><span class="sxs-lookup"><span data-stu-id="9388e-104">Using the File Log</span></span>

<span data-ttu-id="9388e-105">Antes de usar um log de arquivos, você deve chamar [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) para abri-lo ou criá-lo.</span><span class="sxs-lookup"><span data-stu-id="9388e-105">Before you can use a file log, you must call [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) to open or create it.</span></span> <span data-ttu-id="9388e-106">Ao chamar essa função, você pode especificar sinalizadores para criar ou substituir um log de arquivo, abrir o log do sistema ou abrir um log de arquivo como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9388e-106">When you call this function, you can specify flags to create or overwrite a file log, open the system log, or open a file log as read-only.</span></span>

<span data-ttu-id="9388e-107">Depois que o [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) retorna um identificador para um log de arquivo, você pode adicionar uma entrada chamando [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), excluir uma entrada chamando [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)ou recuperar informações sobre um arquivo específico em um log de arquivos chamando [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span><span class="sxs-lookup"><span data-stu-id="9388e-107">After [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) returns a handle to a file log, you can add an entry by calling [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), delete an entry by calling [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya), or retrieve information about a particular file in a file log by calling [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span></span>

<span data-ttu-id="9388e-108">Quando o log de arquivo não for mais necessário, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) deverá ser chamado para liberar os recursos alocados durante a chamada para [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span><span class="sxs-lookup"><span data-stu-id="9388e-108">When the file log is no longer needed, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) should be called to release the resources allocated during the call to [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span></span>

 

 



