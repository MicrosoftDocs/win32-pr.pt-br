---
description: O provedor de política do WMI fornece extensões para a diretiva de grupo por meio de classes, permitindo refinamentos na aplicação da política.
ms.assetid: 5d4d4fd2-ecd0-4546-b919-1e75199a403c
ms.tgt_platform: multiple
title: Classes de provedor de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2e2a142cf677c8f0b14b41ceb5119e71bcfebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749166"
---
# <a name="policy-provider-classes"></a><span data-ttu-id="0ebdd-103">Classes de provedor de política</span><span class="sxs-lookup"><span data-stu-id="0ebdd-103">Policy Provider Classes</span></span>

<span data-ttu-id="0ebdd-104">O provedor de política do WMI fornece extensões para a diretiva de grupo por meio de classes, permitindo refinamentos na aplicação da política.</span><span class="sxs-lookup"><span data-stu-id="0ebdd-104">The WMI policy provider provides extensions to group policy through classes, permitting refinements in the application of policy.</span></span> <span data-ttu-id="0ebdd-105">A política é definida usando o linguagem WQL (WQL) e reside no Active Directory para facilitar a implantação.</span><span class="sxs-lookup"><span data-stu-id="0ebdd-105">Policy is set using the WMI Query Language (WQL) and resides in the Active Directory for easy deployment.</span></span>

<span data-ttu-id="0ebdd-106">A tabela a seguir lista as classes para o provedor de política do WMI.</span><span class="sxs-lookup"><span data-stu-id="0ebdd-106">The following table lists the classes for the WMI policy provider.</span></span>



| <span data-ttu-id="0ebdd-107">Classe</span><span class="sxs-lookup"><span data-stu-id="0ebdd-107">Class</span></span>                                               | <span data-ttu-id="0ebdd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ebdd-108">Description</span></span>                                                       |
|-----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="0ebdd-109">**Provedores de MSFT \_**</span><span class="sxs-lookup"><span data-stu-id="0ebdd-109">**MSFT\_Providers**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-providers) | <span data-ttu-id="0ebdd-110">Expõe a configuração relacionada às instâncias do provedor.</span><span class="sxs-lookup"><span data-stu-id="0ebdd-110">Exposes configuration relating to provider instances.</span></span>             |
| [<span data-ttu-id="0ebdd-111">**\_Regra MSFT**</span><span class="sxs-lookup"><span data-stu-id="0ebdd-111">**MSFT\_Rule**</span></span>](/previous-versions/windows/desktop/policmanprov/msft-rule)                | <span data-ttu-id="0ebdd-112">Define uma única regra dentro de um escopo de gerenciamento (SOM).</span><span class="sxs-lookup"><span data-stu-id="0ebdd-112">Defines a single rule within a Scope of Management (SOM).</span></span>         |
| [<span data-ttu-id="0ebdd-113">**\_SOMFILTER MSFT**</span><span class="sxs-lookup"><span data-stu-id="0ebdd-113">**MSFT\_SomFilter**</span></span>](/previous-versions/windows/desktop/policmanprov/msft-somfilter)      | <span data-ttu-id="0ebdd-114">Fornece uma lista de regras que são avaliadas em um computador de destino.</span><span class="sxs-lookup"><span data-stu-id="0ebdd-114">Provides a list of rules which are evaluated on a target machine.</span></span> |



 

 

 
