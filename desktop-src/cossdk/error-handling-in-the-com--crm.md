---
description: Tratamento de erros no CRM COM+
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Tratamento de erros no CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457057"
---
# <a name="error-handling-in-the-com-crm"></a><span data-ttu-id="4698c-103">Tratamento de erros no CRM COM+</span><span class="sxs-lookup"><span data-stu-id="4698c-103">Error Handling in the COM+ CRM</span></span>

<span data-ttu-id="4698c-104">Aplicativos de servidor COM+ implementam uma política de FailFast.</span><span class="sxs-lookup"><span data-stu-id="4698c-104">COM+ server applications implement a failfast policy.</span></span> <span data-ttu-id="4698c-105">Se um erro interno sério for detectado, o processo do aplicativo do servidor será encerrado e gravará uma mensagem de erro no log de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="4698c-105">If a serious internal error is detected, the server application process exits and writes an error message to the Windows event log.</span></span> <span data-ttu-id="4698c-106">Isso permite a detecção rápida de problemas e é possível devido à proteção dos dados do aplicativo por processamento de transações.</span><span class="sxs-lookup"><span data-stu-id="4698c-106">This allows quick detection of problems and is possible due to the protection of application data by transaction processing.</span></span> <span data-ttu-id="4698c-107">Sempre verifique o log de eventos do Windows em busca de erros do CRM, seja durante o desenvolvimento ou durante a implantação final.</span><span class="sxs-lookup"><span data-stu-id="4698c-107">Always check the Windows event log for any errors from the CRM, either during development or during final deployment.</span></span>

<span data-ttu-id="4698c-108">Erros básicos no uso de interfaces do CRM, como argumentos inválidos ou erros de sequência (por exemplo, tentar gravar um registro de log antes de registrar o compensador de CRM), retornar códigos de erro e não devem disparar FailFast.</span><span class="sxs-lookup"><span data-stu-id="4698c-108">Basic errors in using the CRM interfaces, such as invalid arguments or sequence errors (for example, trying to write a log record before registering the CRM Compensator), return error codes and should not trigger failfast.</span></span> <span data-ttu-id="4698c-109">Para o desenvolvimento de CRM, você pode optar por definir a chave do registro VTRACE1 (consulte [configurações do registro do com+ CRM](com--crm-registry-settings.md)), que faz com que uma mensagem apareça na janela de saída do depurador para cada erro.</span><span class="sxs-lookup"><span data-stu-id="4698c-109">For CRM development, you may choose to set the VTRACE1 registry key (see [COM+ CRM Registry Settings](com--crm-registry-settings.md)), which causes a message to appear in the debugger output window for each error.</span></span>

<span data-ttu-id="4698c-110">Também podem ocorrer erros transitórios.</span><span class="sxs-lookup"><span data-stu-id="4698c-110">Transient errors can also occur.</span></span> <span data-ttu-id="4698c-111">Esses erros geralmente são causados por condições de tempo e resultam em um código de erro retornado.</span><span class="sxs-lookup"><span data-stu-id="4698c-111">These errors are typically caused by timing conditions and result in an error code being returned.</span></span> <span data-ttu-id="4698c-112">O desenvolvedor de CRM deve garantir que essas condições de erro sejam tratadas.</span><span class="sxs-lookup"><span data-stu-id="4698c-112">The CRM developer should ensure that these error conditions are handled.</span></span> <span data-ttu-id="4698c-113">Por exemplo, ao gravar um registro de log, a transação pode abortar devido a um tempo limite. O método, em seguida, retorna um erro, que o chamador deve verificar e tratar adequadamente.</span><span class="sxs-lookup"><span data-stu-id="4698c-113">For example, while writing a log record, the transaction could abort due to a time-out. The method then returns an error, which the caller should check for and handle appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4698c-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4698c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4698c-115">Conceitos do Gerenciador de recursos de compensação COM+</span><span class="sxs-lookup"><span data-stu-id="4698c-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



