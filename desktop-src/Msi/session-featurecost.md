---
description: A propriedade FeatureCost do objeto Session retorna a quantidade total de espaço em disco (em unidades de 512 bytes) exigida pelo recurso especificado e seus recursos pai (até a raiz da tabela de recursos).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Propriedade Session. FeatureCost
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747524"
---
# <a name="sessionfeaturecost-property"></a><span data-ttu-id="d0aa1-103">Propriedade Session. FeatureCost</span><span class="sxs-lookup"><span data-stu-id="d0aa1-103">Session.FeatureCost property</span></span>

<span data-ttu-id="d0aa1-104">A propriedade **FeatureCost** do objeto [**Session**](session-object.md) retorna a quantidade total de espaço em disco (em unidades de 512 bytes) exigida pelo recurso especificado e seus recursos pai (até a raiz da tabela de recursos).</span><span class="sxs-lookup"><span data-stu-id="d0aa1-104">The **FeatureCost** property of the [**Session**](session-object.md) object returns the total amount of disk space (in units of 512 bytes) required by the specified feature and its parent features (up to the root of the Feature table).</span></span> <span data-ttu-id="d0aa1-105">Para cada recurso, o custo total é composto pelos custos de disco atribuídos a todos os componentes vinculados ao recurso.</span><span class="sxs-lookup"><span data-stu-id="d0aa1-105">For each feature, the total cost is made up of the disk costs attributed to every component linked to the feature.</span></span>

<span data-ttu-id="d0aa1-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d0aa1-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0aa1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d0aa1-107">Syntax</span></span>


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a><span data-ttu-id="d0aa1-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d0aa1-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d0aa1-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0aa1-109">Remarks</span></span>

<span data-ttu-id="d0aa1-110">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="d0aa1-110">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0aa1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0aa1-111">Requirements</span></span>



| <span data-ttu-id="d0aa1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0aa1-112">Requirement</span></span> | <span data-ttu-id="d0aa1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d0aa1-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0aa1-114">Versão</span><span class="sxs-lookup"><span data-stu-id="d0aa1-114">Version</span></span><br/> | <span data-ttu-id="d0aa1-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d0aa1-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d0aa1-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d0aa1-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d0aa1-117">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0aa1-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d0aa1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d0aa1-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0aa1-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0aa1-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d0aa1-120">IID</span><span class="sxs-lookup"><span data-stu-id="d0aa1-120">IID</span></span><br/>     | <span data-ttu-id="d0aa1-121">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d0aa1-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




