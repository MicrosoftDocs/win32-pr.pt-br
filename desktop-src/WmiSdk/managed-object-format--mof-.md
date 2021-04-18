---
description: Formato MOF (MOF) é a linguagem usada para descrever as classes de modelo CIM (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: MOF (Managed Object Format)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763214"
---
# <a name="managed-object-format-mof"></a><span data-ttu-id="68cfe-103">MOF (Managed Object Format)</span><span class="sxs-lookup"><span data-stu-id="68cfe-103">Managed Object Format (MOF)</span></span>

<span data-ttu-id="68cfe-104">Formato MOF (MOF) é a linguagem usada para descrever as classes [*de modelo CIM (CIM)*](gloss-c.md) .</span><span class="sxs-lookup"><span data-stu-id="68cfe-104">Managed Object Format (MOF) is the language used to describe [*Common Information Model (CIM)*](gloss-c.md) classes.</span></span>

<span data-ttu-id="68cfe-105">A maneira recomendada para os provedores WMI implementarem novas classes WMI é em arquivos MOF que são compilados usando [**Mofcomp.exe**](mofcomp.md) no [*repositório WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="68cfe-105">The recommended way for WMI providers to implement new WMI classes is in MOF files which are compiled using [**Mofcomp.exe**](mofcomp.md) into the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="68cfe-106">Também é possível criar e manipular classes e instâncias CIM usando a [API com para o WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="68cfe-106">It is also possible to create and manipulate CIM classes and instances using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="68cfe-107">Um provedor WMI normalmente consiste em um arquivo MOF, que define os dados e as classes de evento para os quais o provedor retorna dados e um arquivo DLL que contém o código que fornece dados.</span><span class="sxs-lookup"><span data-stu-id="68cfe-107">A WMI provider normally consists of a MOF file, which defines the data and event classes for which the provider returns data, and a DLL file which contains the code that supplies data.</span></span> <span data-ttu-id="68cfe-108">Para obter mais informações, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="68cfe-108">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="68cfe-109">Os aplicativos e scripts do cliente WMI podem consultar instâncias de classes do provedor MOF ou assinar para receber notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="68cfe-109">WMI client scripts and applications can query for instances of provider MOF classes or subscribe to receive event notifications.</span></span>

<span data-ttu-id="68cfe-110">Você pode executar as seguintes tarefas com o MOF:</span><span class="sxs-lookup"><span data-stu-id="68cfe-110">You can perform the following tasks with MOF:</span></span>

-   [<span data-ttu-id="68cfe-111">Compilando arquivos MOF</span><span class="sxs-lookup"><span data-stu-id="68cfe-111">Compiling MOF Files</span></span>](compiling-mof-files.md)
-   [<span data-ttu-id="68cfe-112">Criando uma classe</span><span class="sxs-lookup"><span data-stu-id="68cfe-112">Creating a Class</span></span>](creating-a-class.md)
-   [<span data-ttu-id="68cfe-113">Criando uma instância</span><span class="sxs-lookup"><span data-stu-id="68cfe-113">Creating an Instance</span></span>](creating-an-instance.md)
-   [<span data-ttu-id="68cfe-114">Criando um método</span><span class="sxs-lookup"><span data-stu-id="68cfe-114">Creating a Method</span></span>](creating-a-method.md)
-   [<span data-ttu-id="68cfe-115">Adicionando um qualificador</span><span class="sxs-lookup"><span data-stu-id="68cfe-115">Adding a Qualifier</span></span>](adding-a-qualifier.md)
-   [<span data-ttu-id="68cfe-116">Criando um comentário</span><span class="sxs-lookup"><span data-stu-id="68cfe-116">Creating a Comment</span></span>](creating-a-comment.md)

## <a name="related-topics"></a><span data-ttu-id="68cfe-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68cfe-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68cfe-118">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="68cfe-118">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



