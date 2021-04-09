---
description: Os desenvolvedores podem estender a infraestrutura WMI desenvolvendo provedores WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Criando provedores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011833"
---
# <a name="creating-wmi-providers"></a><span data-ttu-id="8874d-103">Criando provedores WMI</span><span class="sxs-lookup"><span data-stu-id="8874d-103">Creating WMI Providers</span></span>

<span data-ttu-id="8874d-104">Os desenvolvedores podem estender a infraestrutura WMI desenvolvendo provedores WMI.</span><span class="sxs-lookup"><span data-stu-id="8874d-104">Developers can extend the WMI infrastructure by developing WMI providers.</span></span> <span data-ttu-id="8874d-105">Provedores WMI são objetos COM que implementam um conjunto especificado de interfaces e, até recentemente, foram sempre implementados em C++.</span><span class="sxs-lookup"><span data-stu-id="8874d-105">WMI providers are COM objects that implement a specified set of interfaces and, until recently, were always implemented in C++.</span></span> <span data-ttu-id="8874d-106">Agora você pode usar linguagens gerenciadas como C# para implementar provedores WMI.</span><span class="sxs-lookup"><span data-stu-id="8874d-106">You can now use managed languages like C# to implement WMI providers.</span></span> <span data-ttu-id="8874d-107">A versão 3,5 do .NET Framework introduziu a estrutura de extensões do provedor WMI que torna isso possível.</span><span class="sxs-lookup"><span data-stu-id="8874d-107">Version 3.5 of the .NET framework introduced the WMI Provider Extensions framework that makes this possible.</span></span> <span data-ttu-id="8874d-108">Para saber mais sobre como criar provedores WMI usando essa estrutura, leia o artigo criando [provedores WMI acoplados usando a extensão 2,0 do provedor de WMI.net](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="8874d-108">To learn more about creating WMI providers by using that framework, read the article, [Writing coupled WMI providers using WMI.NET Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).</span></span>

> [!Note]  
> <span data-ttu-id="8874d-109">Você também pode criar um provedor usando a MI (infraestrutura de gerenciamento do Windows), a versão de próxima geração do WMI.</span><span class="sxs-lookup"><span data-stu-id="8874d-109">You can also create a provider using Windows Management Infrastructure (MI), the next-generation version of WMI.</span></span> <span data-ttu-id="8874d-110">Para obter mais informações, consulte [como implementar um provedor de mi](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span><span class="sxs-lookup"><span data-stu-id="8874d-110">For more information, see [How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).</span></span>

 

<span data-ttu-id="8874d-111">A tabela a seguir descreve o conteúdo nesta seção.</span><span class="sxs-lookup"><span data-stu-id="8874d-111">The following table describes the contents in this section.</span></span>



| <span data-ttu-id="8874d-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="8874d-112">Topic</span></span>                                                      | <span data-ttu-id="8874d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="8874d-113">Description</span></span>                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="8874d-114">Fornecendo dados ao WMI</span><span class="sxs-lookup"><span data-stu-id="8874d-114">Providing Data to WMI</span></span>](providing-data-to-wmi.md)         | <span data-ttu-id="8874d-115">Fornece uma visão geral das etapas envolvidas na criação de um provedor WMI.</span><span class="sxs-lookup"><span data-stu-id="8874d-115">Provides an overview of the steps involved in creating a WMI provider.</span></span>         |
| [<span data-ttu-id="8874d-116">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="8874d-116">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md) | <span data-ttu-id="8874d-117">Descreve as tarefas que você deve executar ao criar vários tipos de provedores de WMI.</span><span class="sxs-lookup"><span data-stu-id="8874d-117">Describes tasks you must perform when creating various types of WMI providers.</span></span> |



 

 

 
