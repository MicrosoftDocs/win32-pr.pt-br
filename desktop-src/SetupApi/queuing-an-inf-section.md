---
description: Além de enfileirar as operações de arquivo individualmente, você também pode enfileirar todos os arquivos listados em uma seção INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Enfileirando uma seção INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506102"
---
# <a name="queuing-an-inf-section"></a><span data-ttu-id="dbdb7-103">Enfileirando uma seção INF</span><span class="sxs-lookup"><span data-stu-id="dbdb7-103">Queuing an INF Section</span></span>

<span data-ttu-id="dbdb7-104">Além de enfileirar as operações de arquivo individualmente, você também pode enfileirar todos os arquivos listados em uma seção INF.</span><span class="sxs-lookup"><span data-stu-id="dbdb7-104">In addition to queuing file operations individually, you can also queue all the files listed in an INF section.</span></span>

<span data-ttu-id="dbdb7-105">Você pode colocar em fila todos os arquivos listados em uma seção **copiar arquivos** de um arquivo inf chamando [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span><span class="sxs-lookup"><span data-stu-id="dbdb7-105">You can queue all the files listed in a **Copy Files** section of an INF file by calling [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span></span> <span data-ttu-id="dbdb7-106">Para que essa função seja bem-sucedida, a seção **copiar arquivos** deve estar no formato adequado e o arquivo inf, ou um de seus arquivos anexados, deve conter as seções **SourceDisksFiles** e **SourceDisksNames** .</span><span class="sxs-lookup"><span data-stu-id="dbdb7-106">For this function to be successful, the **Copy Files** section must be in the proper format and the INF file, or one of its appended files, must contain the **SourceDisksFiles** and **SourceDisksNames** sections.</span></span>

<span data-ttu-id="dbdb7-107">Da mesma forma, se você quiser excluir todos os arquivos especificados em uma seção **Excluir arquivos** de um arquivo inf, poderá chamar [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span><span class="sxs-lookup"><span data-stu-id="dbdb7-107">Similarly, if you want to delete all the files specified in a **Delete Files** section of an INF file, you can call [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span></span> <span data-ttu-id="dbdb7-108">Para renomear todos os arquivos em uma seção **renomear arquivos** de um arquivo inf, use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span><span class="sxs-lookup"><span data-stu-id="dbdb7-108">To rename all the files in a **Rename Files** section of an INF file use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span></span>

 

 



