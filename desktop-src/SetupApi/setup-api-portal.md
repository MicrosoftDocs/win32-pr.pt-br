---
description: Instala drivers de dispositivo de programas com um script de configuração e arquivos INF. Escreva um programa de instalação para configuração de dispositivo e instalação de driver. Essa API não é mais recomendada para a finalidade de instalar aplicativos de software.
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: API de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756546"
---
# <a name="setup-api"></a><span data-ttu-id="cabf9-105">API de instalação</span><span class="sxs-lookup"><span data-stu-id="cabf9-105">Setup API</span></span>

## <a name="purpose"></a><span data-ttu-id="cabf9-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="cabf9-106">Purpose</span></span>

<span data-ttu-id="cabf9-107">A API de instalação fornece um conjunto de funções que um aplicativo de instalação chama para executar operações de instalação.</span><span class="sxs-lookup"><span data-stu-id="cabf9-107">The Setup API provides a set of functions that a setup application calls to perform installation operations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="cabf9-108">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="cabf9-108">Where applicable</span></span>

<span data-ttu-id="cabf9-109">Essas funções de instalação estão disponíveis para desenvolver um aplicativo de instalação.</span><span class="sxs-lookup"><span data-stu-id="cabf9-109">These setup functions are available to develop a setup application.</span></span> <span data-ttu-id="cabf9-110">A API de instalação não deve mais ser usada para instalar aplicativos.</span><span class="sxs-lookup"><span data-stu-id="cabf9-110">Setup API should no longer be used for installing applications.</span></span> <span data-ttu-id="cabf9-111">Em vez disso, use o [Windows Installer](/windows/desktop/Msi/windows-installer-portal)para desenvolver instaladores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="cabf9-111">Instead, use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal)for developing application installers.</span></span> <span data-ttu-id="cabf9-112">A API de instalação continua a ser usada para instalar drivers de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cabf9-112">Setup API continues to be used for installing device drivers.</span></span>

<span data-ttu-id="cabf9-113">A API de instalação destina-se ao desenvolvimento de aplicativos de estilo de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="cabf9-113">The Setup API is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cabf9-114">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="cabf9-114">Developer audience</span></span>

<span data-ttu-id="cabf9-115">Um desenvolvedor poderá usar a API de instalação se seu aplicativo de instalação exigir a seguinte funcionalidade:</span><span class="sxs-lookup"><span data-stu-id="cabf9-115">A developer can use the Setup API if their setup application requires the following functionality:</span></span>

-   <span data-ttu-id="cabf9-116">Enfileiramento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="cabf9-116">Queuing of files.</span></span>
-   <span data-ttu-id="cabf9-117">Instalação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="cabf9-117">Installation of files.</span></span>
-   <span data-ttu-id="cabf9-118">Tratamento de erros de instalação e solicitação de mídia.</span><span class="sxs-lookup"><span data-stu-id="cabf9-118">Handling of installation errors and prompting for media.</span></span>
-   <span data-ttu-id="cabf9-119">Atualizando entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="cabf9-119">Updating registry entries.</span></span>
-   <span data-ttu-id="cabf9-120">Registro de arquivos conforme eles são instalados.</span><span class="sxs-lookup"><span data-stu-id="cabf9-120">Logging of files as they are installed.</span></span>
-   <span data-ttu-id="cabf9-121">Armazenamento dos caminhos de origem usados mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="cabf9-121">Storage of the most recently used source paths.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cabf9-122">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="cabf9-122">Run-time requirements</span></span>

<span data-ttu-id="cabf9-123">Para obter informações sobre quais sistemas operacionais são necessários para usar uma função específica, consulte a seção requisitos da documentação da função.</span><span class="sxs-lookup"><span data-stu-id="cabf9-123">For information about which operating systems are required to use a particular function, see the Requirements section of the documentation for the function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cabf9-124">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="cabf9-124">In this section</span></span>



| <span data-ttu-id="cabf9-125">Tópico</span><span class="sxs-lookup"><span data-stu-id="cabf9-125">Topic</span></span>                                 | <span data-ttu-id="cabf9-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="cabf9-126">Description</span></span>                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cabf9-127">Visão geral</span><span class="sxs-lookup"><span data-stu-id="cabf9-127">Overview</span></span>](overview.md)<br/>   | <span data-ttu-id="cabf9-128">Informações gerais sobre a API de instalação.</span><span class="sxs-lookup"><span data-stu-id="cabf9-128">General information about Setup API.</span></span><br/>                                             |
| [<span data-ttu-id="cabf9-129">Referência</span><span class="sxs-lookup"><span data-stu-id="cabf9-129">Reference</span></span>](reference.md)<br/> | <span data-ttu-id="cabf9-130">Documentação de tipos de dados, estruturas, funções e notificações da API de instalação.</span><span class="sxs-lookup"><span data-stu-id="cabf9-130">Documentation of Setup API data types, structures, functions, and notifications.</span></span><br/> |



 

 

