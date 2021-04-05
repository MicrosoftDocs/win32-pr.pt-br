---
title: Kit de certificação de hardware do Windows
description: Kit de certificação de hardware do Windows
ms.assetid: 99BD2D7D-8F9D-445E-AE04-6A58FFF3DCE6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba820d62d6766f74549ed23f7a5abdccbca258b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008495"
---
# <a name="windows-hardware-certification-kit"></a><span data-ttu-id="16747-103">Kit de certificação de hardware do Windows</span><span class="sxs-lookup"><span data-stu-id="16747-103">Windows Hardware Certification Kit</span></span>

## <a name="platforms"></a><span data-ttu-id="16747-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="16747-104">Platforms</span></span>

 <span data-ttu-id="16747-105">**Clientes** -Windows 7 Windows \| 8</span><span class="sxs-lookup"><span data-stu-id="16747-105">**Clients** - Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="16747-106">**Servidores** -windows Server 2008 R2 \| Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16747-106">**Servers** - Windows Server 2008 R2 \| Windows Server 2012</span></span>  
<span data-ttu-id="16747-107">**Servidor/controlador** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16747-107">**Server/Controller** - Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="16747-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="16747-108">Description</span></span>

<span data-ttu-id="16747-109">O kit de certificação de hardware do Windows permite que desenvolvedores, ISVs, IHVs e OEMs certificem seus dispositivos de hardware, sistemas e drivers de filtro para os sistemas operacionais Windows mais recentes.</span><span class="sxs-lookup"><span data-stu-id="16747-109">The Windows Hardware Certification Kit enables developers, ISVs, IHVs, and OEMs to certify their hardware devices, systems, and filter drivers for the latest Windows operating systems.</span></span> <span data-ttu-id="16747-110">Ele contém todas as ferramentas e a documentação de que você precisa para certificar seus drivers de hardware e filtro para esses sistemas operacionais:</span><span class="sxs-lookup"><span data-stu-id="16747-110">It contains all the tools and documentation that you need to certify your hardware and filter drivers for these operating systems:</span></span>

-   <span data-ttu-id="16747-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="16747-111">Windows 8</span></span>
-   <span data-ttu-id="16747-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16747-112">Windows Server 2012</span></span>
-   <span data-ttu-id="16747-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="16747-113">Windows 7</span></span>
-   <span data-ttu-id="16747-114">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="16747-114">Windows Server 2008 R2</span></span>

<span data-ttu-id="16747-115">O kit de certificação de hardware do Windows substitui o kit de logotipo do Windows e faz parte do programa de certificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="16747-115">The Windows Hardware Certification Kit replaces the Windows Logo Kit and is a part of the Windows Certification Program.</span></span>

## <a name="usage-or-best-practices"></a><span data-ttu-id="16747-116">Uso ou práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="16747-116">Usage or best practices</span></span>

<span data-ttu-id="16747-117">Antes de poder testar qualquer driver de hardware ou de filtro, você deve configurar o ambiente de teste adequado com base no driver de filtro ou hardware que você está certificando.</span><span class="sxs-lookup"><span data-stu-id="16747-117">Before you can test any hardware or filter driver, you must set up the proper test environment based on the hardware or filter driver you are certifying.</span></span> <span data-ttu-id="16747-118">Isso inclui o controlador, o cliente e o hardware potencialmente adicional (por exemplo, dispositivos com várias funções) ou software.</span><span class="sxs-lookup"><span data-stu-id="16747-118">This includes the controller, client, and potentially additional hardware (for example, multi-function devices) or software.</span></span> <span data-ttu-id="16747-119">Depois que o ambiente estiver configurado, você poderá testar seu hardware usando a nova ferramenta do HCK Studio.</span><span class="sxs-lookup"><span data-stu-id="16747-119">After your environment is set up, you can test your hardware using the new HCK’s Studio tool.</span></span> <span data-ttu-id="16747-120">Estas etapas descrevem o processo de teste de certificação.</span><span class="sxs-lookup"><span data-stu-id="16747-120">These steps outline the certification test process.</span></span>

1.  <span data-ttu-id="16747-121">Configurar ambiente de teste.</span><span class="sxs-lookup"><span data-stu-id="16747-121">Set up test environment.</span></span>
2.  <span data-ttu-id="16747-122">Criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="16747-122">Create a project.</span></span>
3.  <span data-ttu-id="16747-123">Crie um ou mais pools de computadores.</span><span class="sxs-lookup"><span data-stu-id="16747-123">Create one or more machine pools.</span></span>
4.  <span data-ttu-id="16747-124">Selecione os recursos a serem validados.</span><span class="sxs-lookup"><span data-stu-id="16747-124">Select features to validate.</span></span>
5.  <span data-ttu-id="16747-125">Selecione e execute testes nesses recursos.</span><span class="sxs-lookup"><span data-stu-id="16747-125">Select and run tests against those features.</span></span>
6.  <span data-ttu-id="16747-126">Exibir resultados de teste.</span><span class="sxs-lookup"><span data-stu-id="16747-126">View test results.</span></span>
7.  <span data-ttu-id="16747-127">Envie seu pacote.</span><span class="sxs-lookup"><span data-stu-id="16747-127">Submit your package.</span></span>

## <a name="resources"></a><span data-ttu-id="16747-128">Recursos</span><span class="sxs-lookup"><span data-stu-id="16747-128">Resources</span></span>

-   [<span data-ttu-id="16747-129">Desenvolvimento de hardware do Windows</span><span class="sxs-lookup"><span data-stu-id="16747-129">Windows Hardware Development</span></span>](https://msdn.microsoft.com/windows/hardware/)
-   <span data-ttu-id="16747-130">[Programa de certificação de hardware do Windows](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="16747-130">[Windows Hardware Certification Program](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span></span>
-   <span data-ttu-id="16747-131">[Iniciar o desenvolvimento de hardware para Windows](/previous-versions/gg507680(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="16747-131">[Start Developing Hardware for Windows](/previous-versions/gg507680(v=msdn.10))</span></span>

 

 