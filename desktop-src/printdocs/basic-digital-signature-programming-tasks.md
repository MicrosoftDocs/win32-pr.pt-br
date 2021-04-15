---
description: Esta seção descreve como executar tarefas básicas de programação com a API de assinatura digital XPS.
ms.assetid: a25a8d33-000a-4774-8beb-56d3bb39d5ae
title: Tarefas comuns de programação de assinatura digital
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346b29c7768f4c4e972284afa697f97bb1da5f69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461330"
---
# <a name="common-digital-signature-programming-tasks"></a><span data-ttu-id="1b2b7-103">Tarefas comuns de programação de assinatura digital</span><span class="sxs-lookup"><span data-stu-id="1b2b7-103">Common Digital Signature Programming Tasks</span></span>

<span data-ttu-id="1b2b7-104">Esta seção descreve como executar tarefas básicas de programação com a API de assinatura digital XPS.</span><span class="sxs-lookup"><span data-stu-id="1b2b7-104">This section describes how to perform basic programming tasks with the XPS Digital Signature API.</span></span>

<span data-ttu-id="1b2b7-105">Tarefas</span><span class="sxs-lookup"><span data-stu-id="1b2b7-105">Tasks</span></span>

-   [<span data-ttu-id="1b2b7-106">Inicializar o Gerenciador de assinatura</span><span class="sxs-lookup"><span data-stu-id="1b2b7-106">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)
-   [<span data-ttu-id="1b2b7-107">Assinar um documento</span><span class="sxs-lookup"><span data-stu-id="1b2b7-107">Sign a Document</span></span>](sign-a-document.md)
-   [<span data-ttu-id="1b2b7-108">Adicionar uma solicitação de assinatura a um documento XPS</span><span class="sxs-lookup"><span data-stu-id="1b2b7-108">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
-   [<span data-ttu-id="1b2b7-109">Verificar assinaturas de documento</span><span class="sxs-lookup"><span data-stu-id="1b2b7-109">Verify Document Signatures</span></span>](verify-document-signatures.md)

## <a name="disclaimer"></a><span data-ttu-id="1b2b7-110">Isenção de responsabilidade</span><span class="sxs-lookup"><span data-stu-id="1b2b7-110">Disclaimer</span></span>

<span data-ttu-id="1b2b7-111">Os exemplos de código não se destinam a serem programas completos e em funcionamento.</span><span class="sxs-lookup"><span data-stu-id="1b2b7-111">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="1b2b7-112">Os exemplos de código que são referenciados nesta página, por exemplo, não executam a verificação de parâmetros, verificação de erros, memória completa ou gerenciamento de recursos ou tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="1b2b7-112">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, complete memory or resource management, or error handling.</span></span> <span data-ttu-id="1b2b7-113">Use estes exemplos como ponto de partida e, em seguida, adicione o código necessário para criar um aplicativo robusto.</span><span class="sxs-lookup"><span data-stu-id="1b2b7-113">Use these examples as a starting point, then add the necessary code to create a robust application.</span></span> <span data-ttu-id="1b2b7-114">Para obter mais informações sobre valores de retorno **HRESULT** e estratégias de tratamento de erros, consulte [tratamento de erros em com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="1b2b7-114">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="1b2b7-115">Para maior clareza, esses exemplos de código usam cenários de documento e assinatura XPS muito simples, que podem não ser suficientemente complexos para atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="1b2b7-115">For clarity, these code examples use very simple XPS document and signature scenarios, which might not be sufficiently complex to meet your needs.</span></span>

 

 
