---
description: Ao usar CSPs de provedores de serviço de criptografia, tenha em mente as convenções a seguir.
ms.assetid: 70053b89-4d39-4a86-985a-0e8f05fbc9c0
title: 'Usando CSPs: processos gerais'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93f067ef0e3cd837b1b347daac3e3da21543047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784138"
---
# <a name="using-csps-general-processes"></a><span data-ttu-id="870ae-103">Usando CSPs: processos gerais</span><span class="sxs-lookup"><span data-stu-id="870ae-103">Using CSPs: General Processes</span></span>

<span data-ttu-id="870ae-104">Ao usar CSPs de [*provedores de serviço de criptografia*](../secgloss/c-gly.md) , tenha em mente as convenções a seguir.</span><span class="sxs-lookup"><span data-stu-id="870ae-104">When using [*cryptographic service providers*](../secgloss/c-gly.md) CSPs, keep the following conventions in mind.</span></span>

## <a name="private-key-caching"></a><span data-ttu-id="870ae-105">Cache de chave privada</span><span class="sxs-lookup"><span data-stu-id="870ae-105">Private Key Caching</span></span>

<span data-ttu-id="870ae-106">Um CSP pode armazenar em cache algumas [*chaves privadas*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="870ae-106">A CSP can cache some [*private keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="870ae-107">É possível controlar esse cache de chave privada em um global, mas não em um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="870ae-107">It is possible to control this private key caching on a global, but not an application-specific, basis.</span></span> <span data-ttu-id="870ae-108">As alterações de cache são feitas modificando determinadas configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="870ae-108">Caching changes are made by modifying certain registry settings.</span></span> <span data-ttu-id="870ae-109">Para obter mais informações, consulte [**constantes de cache de chave privada**](private-key-caching-constants.md).</span><span class="sxs-lookup"><span data-stu-id="870ae-109">For more information, see [**Private Key Caching Constants**](private-key-caching-constants.md).</span></span>

## <a name="example-code-conventions"></a><span data-ttu-id="870ae-110">Convenções de código de exemplo</span><span class="sxs-lookup"><span data-stu-id="870ae-110">Example Code Conventions</span></span>

<span data-ttu-id="870ae-111">Para fornecer um código mais conciso e mais legível, alguns princípios da boa prática de programação nem sempre são seguidos nos exemplos.</span><span class="sxs-lookup"><span data-stu-id="870ae-111">To provide more concise, more readable code, some principles of good programming practice are not always followed in the examples.</span></span> <span data-ttu-id="870ae-112">Especialmente:</span><span class="sxs-lookup"><span data-stu-id="870ae-112">In particular:</span></span>

-   <span data-ttu-id="870ae-113">Somente respostas de erro limitadas são mostradas.</span><span class="sxs-lookup"><span data-stu-id="870ae-113">Only limited error responses are shown.</span></span> <span data-ttu-id="870ae-114">Bem-escrito, os programas completos verificam os códigos de erro e executam as ações apropriadas quando um erro é encontrado.</span><span class="sxs-lookup"><span data-stu-id="870ae-114">Well-written, complete programs check returned error codes and perform appropriate actions when an error is encountered.</span></span>
-   <span data-ttu-id="870ae-115">Somente a memória limitada e o gerenciamento de recursos são feitos.</span><span class="sxs-lookup"><span data-stu-id="870ae-115">Only limited memory and resource management is done.</span></span> <span data-ttu-id="870ae-116">Bem-escrito, programas completos destrói todas as chaves e [*hashes*](../secgloss/h-gly.md), liberam toda a memória alocada, fecham todos os arquivos e liberam todos os identificadores.</span><span class="sxs-lookup"><span data-stu-id="870ae-116">Well-written, complete programs destroy all keys and [*hashes*](../secgloss/h-gly.md), free all allocated memory, close all files, and release all handles.</span></span> <span data-ttu-id="870ae-117">Esses exemplos fornecem apenas demonstrações limitadas do uso de funções que executam essas tarefas.</span><span class="sxs-lookup"><span data-stu-id="870ae-117">These examples provide only limited demonstrations of the use of functions that perform these tasks.</span></span> <span data-ttu-id="870ae-118">Esses exemplos não executam nenhuma tarefa de gerenciamento de recursos ou memória no caso de encerramento do programa devido a erros.</span><span class="sxs-lookup"><span data-stu-id="870ae-118">These examples perform no memory or resource management tasks in the case of program termination due to errors.</span></span>

<span data-ttu-id="870ae-119">Os tópicos a seguir apresentam informações gerais sobre exemplos de procedimento, bem como código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="870ae-119">The following topics present general information about procedure examples as well as sample code.</span></span>

-   [<span data-ttu-id="870ae-120">Recuperando dados de comprimento desconhecido</span><span class="sxs-lookup"><span data-stu-id="870ae-120">Retrieving Data of Unknown Length</span></span>](retrieving-data-of-unknown-length.md)
-   [<span data-ttu-id="870ae-121">Enumerando protocolos com suporte</span><span class="sxs-lookup"><span data-stu-id="870ae-121">Enumerating Supported Protocols</span></span>](enumerating-supported-protocols.md)

 

 
