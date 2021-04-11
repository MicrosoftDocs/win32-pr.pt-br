---
title: Compartilhando um procedimento de e/s com outros aplicativos
description: Compartilhando um procedimento de e/s com outros aplicativos
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- e/s de arquivo multimídia, procedimentos compartilhados
- e/s de arquivo, procedimentos compartilhados
- entrada e saída (e/s), procedimentos compartilhados
- E/s (entrada e saída), procedimentos compartilhados
- compartilhando procedimentos de e/s com outros aplicativos
- função mmioInstallIOProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365894"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a><span data-ttu-id="a9004-109">Compartilhando um procedimento de e/s com outros aplicativos</span><span class="sxs-lookup"><span data-stu-id="a9004-109">Sharing an I/O Procedure with Other Applications</span></span>

<span data-ttu-id="a9004-110">Se desejar compartilhar um procedimento de e/s com outros aplicativos, você precisará gravar uma DLL (biblioteca de vínculo dinâmico) para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a9004-110">If you want to share an I/O procedure with other applications, you need to write a dynamic-link library (DLL) for your application.</span></span> <span data-ttu-id="a9004-111">Você pode compartilhar o procedimento de e/s seguindo um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="a9004-111">You can share the I/O procedure by doing one of the following:</span></span>

-   <span data-ttu-id="a9004-112">Inclua o código para o procedimento de e/s na DLL.</span><span class="sxs-lookup"><span data-stu-id="a9004-112">Include the code for the I/O procedure in the DLL.</span></span>
-   <span data-ttu-id="a9004-113">Crie uma função na DLL que chama a função [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) para instalar o procedimento de e/s.</span><span class="sxs-lookup"><span data-stu-id="a9004-113">Create a function in the DLL that calls the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function to install the I/O procedure.</span></span>
-   <span data-ttu-id="a9004-114">Exporte essa função no arquivo de definições de módulo da DLL.</span><span class="sxs-lookup"><span data-stu-id="a9004-114">Export this function in the module-definitions file of the DLL.</span></span>

<span data-ttu-id="a9004-115">Para usar o procedimento de e/s compartilhado, um aplicativo deve primeiro chamar a função na DLL para instalar o procedimento de e/s.</span><span class="sxs-lookup"><span data-stu-id="a9004-115">To use the shared I/O procedure, an application must first call the function in the DLL to install the I/O procedure.</span></span>

 

 