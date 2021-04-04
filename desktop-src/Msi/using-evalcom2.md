---
description: Evalcom2.dll pode ser usado para implementar operações de validação para pacotes de instalação e módulos de mesclagem usando avaliadores de consistência internos-ICEs.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Usando Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647198"
---
# <a name="using-evalcom2"></a><span data-ttu-id="180d7-103">Usando Evalcom2</span><span class="sxs-lookup"><span data-stu-id="180d7-103">Using Evalcom2</span></span>

<span data-ttu-id="180d7-104">Evalcom2.dll pode ser usado para implementar operações de validação para pacotes de instalação e módulos de mesclagem usando [avaliadores de consistência internos-ICES](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="180d7-104">Evalcom2.dll can be used to implement validation operations for installation packages and merge modules using [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="180d7-105">O objeto principal implementa interfaces para programas C/C++.</span><span class="sxs-lookup"><span data-stu-id="180d7-105">The main object implements interfaces for C/C++ programs.</span></span>

<span data-ttu-id="180d7-106">O objeto principal também implementa [interfaces Evalcom2](evalcom2-interfaces.md) para programas C/C++.</span><span class="sxs-lookup"><span data-stu-id="180d7-106">The main object also implements [Evalcom2 interfaces](evalcom2-interfaces.md) for C/C++ programs.</span></span> <span data-ttu-id="180d7-107">O CLSID necessário para obter a interface de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) é {6E5E1910-8053-4660-B795-6B612E29BC58}.</span><span class="sxs-lookup"><span data-stu-id="180d7-107">The CLSID required to obtain the interface from [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is {6E5E1910-8053-4660-B795-6B612E29BC58}.</span></span> <span data-ttu-id="180d7-108">O REFIID é {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span><span class="sxs-lookup"><span data-stu-id="180d7-108">The REFIID is {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span></span>

<span data-ttu-id="180d7-109">Você pode usar o procedimento a seguir para implementar operações de validação.</span><span class="sxs-lookup"><span data-stu-id="180d7-109">You can use the following procedure to implement validation operations.</span></span>

<span data-ttu-id="180d7-110">**Para implementar operações de validação**</span><span class="sxs-lookup"><span data-stu-id="180d7-110">**To implement validation operations**</span></span>

1.  <span data-ttu-id="180d7-111">Inicialize COM no thread de chamada usando o [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="180d7-111">Initialize COM on the calling thread using [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span></span>
2.  <span data-ttu-id="180d7-112">Obtenha o ponteiro para a interface [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) usando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="180d7-112">Obtain the pointer to the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>
3.  <span data-ttu-id="180d7-113">Abra o pacote de instalação ou o módulo de mesclagem usando o método [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) .</span><span class="sxs-lookup"><span data-stu-id="180d7-113">Open the installation package or merge module using the [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) method.</span></span>
4.  <span data-ttu-id="180d7-114">Abra o arquivo de avaliação usando o método [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) .</span><span class="sxs-lookup"><span data-stu-id="180d7-114">Open the evaluation file using the [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) method.</span></span>
5.  <span data-ttu-id="180d7-115">Defina a função de retorno de chamada de exibição usando o método [**setdisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) .</span><span class="sxs-lookup"><span data-stu-id="180d7-115">Set the display callback function using the [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) method.</span></span>
6.  <span data-ttu-id="180d7-116">Defina a função de retorno de chamada de status usando o método [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="180d7-116">Set the status callback function using the [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) method.</span></span>
7.  <span data-ttu-id="180d7-117">Execute a validação usando o método [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) .</span><span class="sxs-lookup"><span data-stu-id="180d7-117">Perform the validation using the [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) method.</span></span>
8.  <span data-ttu-id="180d7-118">Feche o arquivo. Cub usando o método [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) .</span><span class="sxs-lookup"><span data-stu-id="180d7-118">Close the .cub file using the [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) method.</span></span>
9.  <span data-ttu-id="180d7-119">Feche o banco de dados usando o método [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) .</span><span class="sxs-lookup"><span data-stu-id="180d7-119">Close the database using the [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) method.</span></span>
10. <span data-ttu-id="180d7-120">Libere a interface [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) .</span><span class="sxs-lookup"><span data-stu-id="180d7-120">Release the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface.</span></span>
11. <span data-ttu-id="180d7-121">Não inicializar COM usando [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="180d7-121">Uninitialize COM using [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

## <a name="related-topics"></a><span data-ttu-id="180d7-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="180d7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="180d7-123">Interfaces Evalcom2</span><span class="sxs-lookup"><span data-stu-id="180d7-123">Evalcom2 Interfaces</span></span>](evalcom2-interfaces.md)
</dt> <dt>

[<span data-ttu-id="180d7-124">Automação de validação</span><span class="sxs-lookup"><span data-stu-id="180d7-124">Validation Automation</span></span>](validation-automation.md)
</dt> <dt>

[<span data-ttu-id="180d7-125">Funções de retorno de chamada de validação</span><span class="sxs-lookup"><span data-stu-id="180d7-125">Validation Callback Functions</span></span>](validation-callback-functions.md)
</dt> </dl>

 

 
