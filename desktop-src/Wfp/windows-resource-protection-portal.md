---
description: A proteção de recursos impede a substituição de arquivos e pastas do sistema e chaves do registro essenciais para o sistema operacional. A modificação de recursos protegidos pode causar falha no aplicativo ou no sistema.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Proteção de Recursos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297092"
---
# <a name="windows-resource-protection"></a><span data-ttu-id="ab34e-104">Proteção de Recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="ab34e-104">Windows Resource Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="ab34e-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="ab34e-105">Purpose</span></span>

<span data-ttu-id="ab34e-106">O Proteção de Recursos do Windows (WRP) impede a substituição de arquivos de sistema, pastas e chaves do registro essenciais que são instalados como parte do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ab34e-106">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="ab34e-107">Ele se tornou disponível a partir do Windows Server 2008 e do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ab34e-107">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="ab34e-108">Os aplicativos não devem substituir esses recursos porque eles são usados pelo sistema e por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ab34e-108">Applications should not overwrite these resources because they are used by the system and other applications.</span></span> <span data-ttu-id="ab34e-109">A proteção desses recursos impede falhas de aplicativos e do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ab34e-109">Protecting these resources prevents application and operating system failures.</span></span> <span data-ttu-id="ab34e-110">WRP é o novo nome da WFP (proteção de arquivo do Windows).</span><span class="sxs-lookup"><span data-stu-id="ab34e-110">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="ab34e-111">A WRP protege chaves e pastas do registro, bem como arquivos essenciais do sistema.</span><span class="sxs-lookup"><span data-stu-id="ab34e-111">WRP protects registry keys and folders as well as essential system files.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="ab34e-112">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="ab34e-112">Where applicable</span></span>

<span data-ttu-id="ab34e-113">Todos os aplicativos baseados no Windows e seus programas de instalação executados no Windows Server 2008 ou no Windows Vista e em sistemas operacionais posteriores devem estar cientes da WRP.</span><span class="sxs-lookup"><span data-stu-id="ab34e-113">All Windows-based applications and their installation programs that run on Windows Server 2008 or Windows Vista, and later operating systems, should be aware of WRP.</span></span> <span data-ttu-id="ab34e-114">Todos os aplicativos baseados no Windows que são executados no Microsoft Windows Server 2003 ou no Windows XP e seus programas de instalação devem estar cientes do WFP.</span><span class="sxs-lookup"><span data-stu-id="ab34e-114">All Windows-based applications that run on Microsoft Windows Server 2003 or Windows XP and their installation programs should be aware of WFP.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ab34e-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="ab34e-115">Developer audience</span></span>

<span data-ttu-id="ab34e-116">A API WRP foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="ab34e-116">The WRP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="ab34e-117">A API WRP tem duas funções: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span><span class="sxs-lookup"><span data-stu-id="ab34e-117">The WRP API has two functions: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ab34e-118">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="ab34e-118">Run-time requirements</span></span>

<span data-ttu-id="ab34e-119">Os aplicativos que usam apenas a função [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) exigem o windows Server 2008, o Windows Vista, o windows Server 2003 ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab34e-119">Applications that use only the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) function require Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP.</span></span> <span data-ttu-id="ab34e-120">Os aplicativos que usam a função [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) exigem o windows Server 2008 ou o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ab34e-120">Applications that use the [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) function require Windows Server 2008 or Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ab34e-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ab34e-121">In this section</span></span>



| <span data-ttu-id="ab34e-122">Tópico</span><span class="sxs-lookup"><span data-stu-id="ab34e-122">Topic</span></span>                                                                                     | <span data-ttu-id="ab34e-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab34e-123">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="ab34e-124">Sobre Proteção de Recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="ab34e-124">About Windows Resource Protection</span></span>](about-windows-file-protection.md)<br/>         | <span data-ttu-id="ab34e-125">Informações gerais sobre WRP.</span><span class="sxs-lookup"><span data-stu-id="ab34e-125">General information about WRP.</span></span><br/>   |
| [<span data-ttu-id="ab34e-126">Referência de Proteção de Recursos do Windows</span><span class="sxs-lookup"><span data-stu-id="ab34e-126">Windows Resource Protection Reference</span></span>](windows-file-protection-reference.md)<br/> | <span data-ttu-id="ab34e-127">Documentação de referência para WRP.</span><span class="sxs-lookup"><span data-stu-id="ab34e-127">Reference documentation for WRP.</span></span><br/> |



 

 

 




