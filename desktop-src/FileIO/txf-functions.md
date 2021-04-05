---
description: Funções de NTFS Transacional (TxF).
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: Funções TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662932"
---
# <a name="txf-functions"></a><span data-ttu-id="ff096-103">Funções TxF</span><span class="sxs-lookup"><span data-stu-id="ff096-103">TxF Functions</span></span>

<span data-ttu-id="ff096-104">O NTFS Transacional (TxF) fornece as funções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ff096-104">Transactional NTFS (TxF) provides the following functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ff096-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ff096-105">In this section</span></span>



| <span data-ttu-id="ff096-106">Função</span><span class="sxs-lookup"><span data-stu-id="ff096-106">Function</span></span>                                                                      | <span data-ttu-id="ff096-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff096-107">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff096-108">**TxfLogCreateFileReadContext**</span><span class="sxs-lookup"><span data-stu-id="ff096-108">**TxfLogCreateFileReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | <span data-ttu-id="ff096-109">Cria um contexto a ser usado para ler registros de replicação.</span><span class="sxs-lookup"><span data-stu-id="ff096-109">Creates a context to be used to read replication records.</span></span><br/>                                                         |
| [<span data-ttu-id="ff096-110">**TxfLogDestroyReadContext**</span><span class="sxs-lookup"><span data-stu-id="ff096-110">**TxfLogDestroyReadContext**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | <span data-ttu-id="ff096-111">Fecha um contexto de leitura criado pela função [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) .</span><span class="sxs-lookup"><span data-stu-id="ff096-111">Closes a read context created by the [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) function.</span></span><br/> |
| [<span data-ttu-id="ff096-112">**TxfLogReadRecords**</span><span class="sxs-lookup"><span data-stu-id="ff096-112">**TxfLogReadRecords**</span></span>](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | <span data-ttu-id="ff096-113">Lê os registros refazer do log.</span><span class="sxs-lookup"><span data-stu-id="ff096-113">Reads the redo records from the log.</span></span><br/>                                                                              |



 

 

 




