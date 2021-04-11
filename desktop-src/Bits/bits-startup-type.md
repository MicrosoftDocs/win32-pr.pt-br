---
title: Tipo de inicialização do BITS
description: O tipo de inicialização para BITS é um início automático atrasado. Antes do Windows Vista, o tipo de inicialização para BITS é manual. Quando um trabalho do BITS é criado, o tipo de inicialização muda para automático. O tipo de inicialização retorna para manual quando todos os trabalhos são concluídos ou cancelados.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1ce1dcd2f939237142a0afd44e49b4b63df419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363687"
---
# <a name="bits-startup-type"></a><span data-ttu-id="2f820-106">Tipo de inicialização do BITS</span><span class="sxs-lookup"><span data-stu-id="2f820-106">BITS Startup Type</span></span>

<span data-ttu-id="2f820-107">O **tipo de inicialização** para bits é o início automático atrasado (se houver trabalhos bits ativos) ou início da demanda (se não houver trabalhos ativos).</span><span class="sxs-lookup"><span data-stu-id="2f820-107">The **Startup Type** for BITS is delayed auto-start (if there are active BITS jobs) or demand start (if there are no active jobs).</span></span> <span data-ttu-id="2f820-108">Versões do Windows anteriores à atualização de novembro usaram apenas o tipo de inicialização de início automático atrasado; versões anteriores ao vista usaram o tipo de inicialização manual.</span><span class="sxs-lookup"><span data-stu-id="2f820-108">Versions of Windows prior to the November Update used only the delayed auto-start startup type; versions prior to Vista used the manual startup type.</span></span>

<span data-ttu-id="2f820-109">Você não deve definir o **tipo de inicialização** como desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2f820-109">You should not set the **Startup Type** to Disabled.</span></span> <span data-ttu-id="2f820-110">Desabilitar BITS pode interromper aplicativos que dependem de BITS para transferir arquivos.</span><span class="sxs-lookup"><span data-stu-id="2f820-110">Disabling BITS may break applications that rely on BITS to transfer files.</span></span>

 

 




