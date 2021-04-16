---
description: A propriedade VerifyDiskSpace é uma propriedade somente leitura.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Propriedade Session. VerifyDiskSpace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768718"
---
# <a name="sessionverifydiskspace-property"></a><span data-ttu-id="5c6d6-103">Propriedade Session. VerifyDiskSpace</span><span class="sxs-lookup"><span data-stu-id="5c6d6-103">Session.VerifyDiskSpace property</span></span>

<span data-ttu-id="5c6d6-104">A propriedade **VerifyDiskSpace** é uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5c6d6-104">The **VerifyDiskSpace** property is a read-only property.</span></span> <span data-ttu-id="5c6d6-105">Retornará true se houver espaço em disco suficiente e false se o disco estiver cheio.</span><span class="sxs-lookup"><span data-stu-id="5c6d6-105">It returns true if enough disk space exists and false if the disk is full.</span></span> <span data-ttu-id="5c6d6-106">Como essa propriedade usa as informações coletadas pelas ações de custo, **VerifyDiskSpace** deve ser chamado somente após a ação [CostInitialize](costinitialize-action.md), a ação de [filecusto](filecost-action.md)e a ação [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="5c6d6-106">Because this property uses information gathered by the costing actions, **VerifyDiskSpace** should only be called after the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="5c6d6-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5c6d6-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c6d6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c6d6-108">Syntax</span></span>


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a><span data-ttu-id="5c6d6-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5c6d6-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="5c6d6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c6d6-110">Requirements</span></span>



| <span data-ttu-id="5c6d6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c6d6-111">Requirement</span></span> | <span data-ttu-id="5c6d6-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5c6d6-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6d6-113">Versão</span><span class="sxs-lookup"><span data-stu-id="5c6d6-113">Version</span></span><br/> | <span data-ttu-id="5c6d6-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c6d6-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5c6d6-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5c6d6-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5c6d6-116">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5c6d6-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5c6d6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="5c6d6-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c6d6-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c6d6-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5c6d6-119">IID</span><span class="sxs-lookup"><span data-stu-id="5c6d6-119">IID</span></span><br/>     | <span data-ttu-id="5c6d6-120">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5c6d6-120">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




