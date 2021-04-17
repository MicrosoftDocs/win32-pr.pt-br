---
description: A propriedade ComponentRequestState do objeto Session Obtém ou solicita uma alteração no estado de ação de uma linha na tabela de componentes.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Propriedade Session. ComponentRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766386"
---
# <a name="sessioncomponentrequeststate-property"></a><span data-ttu-id="b136f-103">Propriedade Session. ComponentRequestState</span><span class="sxs-lookup"><span data-stu-id="b136f-103">Session.ComponentRequestState property</span></span>

<span data-ttu-id="b136f-104">A propriedade **ComponentRequestState** do objeto [**Session**](session-object.md) Obtém ou solicita uma alteração no estado de ação de uma linha na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b136f-104">The **ComponentRequestState** property of the [**Session**](session-object.md) object obtains or requests a change in the Action state of a row in the [Component table](component-table.md).</span></span>

<span data-ttu-id="b136f-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b136f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b136f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b136f-106">Syntax</span></span>


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a><span data-ttu-id="b136f-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b136f-107">Property value</span></span>

<span data-ttu-id="b136f-108">Nome de cadeia de caracteres necessário do item de componente, chave primária da tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="b136f-108">Required string name of the component item, primary key of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="b136f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b136f-109">Remarks</span></span>



| <span data-ttu-id="b136f-110">Estado da seleção</span><span class="sxs-lookup"><span data-stu-id="b136f-110">Selection state</span></span>        | <span data-ttu-id="b136f-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b136f-111">Value</span></span> | <span data-ttu-id="b136f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b136f-112">Description</span></span>                                                    |
|------------------------|-------|----------------------------------------------------------------|
| <span data-ttu-id="b136f-113">Nulo</span><span class="sxs-lookup"><span data-stu-id="b136f-113">Null</span></span>                   | <span data-ttu-id="b136f-114">Nulo</span><span class="sxs-lookup"><span data-stu-id="b136f-114">Null</span></span>  | <span data-ttu-id="b136f-115">Solicita que nenhuma ação seja executada para este item.</span><span class="sxs-lookup"><span data-stu-id="b136f-115">Requests that no action be taken for this item.</span></span>                |
| <span data-ttu-id="b136f-116">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="b136f-116">msiInstallStateAbsent</span></span>  | <span data-ttu-id="b136f-117">2</span><span class="sxs-lookup"><span data-stu-id="b136f-117">2</span></span>     | <span data-ttu-id="b136f-118">O item deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="b136f-118">Item is to be removed.</span></span>                                         |
| <span data-ttu-id="b136f-119">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="b136f-119">msiInstallStateLocal</span></span>   | <span data-ttu-id="b136f-120">3</span><span class="sxs-lookup"><span data-stu-id="b136f-120">3</span></span>     | <span data-ttu-id="b136f-121">O item deve ser instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="b136f-121">Item is to be installed locally.</span></span>                               |
| <span data-ttu-id="b136f-122">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="b136f-122">msiInstallStateSource</span></span>  | <span data-ttu-id="b136f-123">4</span><span class="sxs-lookup"><span data-stu-id="b136f-123">4</span></span>     | <span data-ttu-id="b136f-124">O item deve ser instalado e executado a partir da mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="b136f-124">Item is to be installed and run from the source media.</span></span>         |
| <span data-ttu-id="b136f-125">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="b136f-125">msiInstallStateDefault</span></span> | <span data-ttu-id="b136f-126">5</span><span class="sxs-lookup"><span data-stu-id="b136f-126">5</span></span>     | <span data-ttu-id="b136f-127">Se instalado, o item será reinstalado no mesmo estado.</span><span class="sxs-lookup"><span data-stu-id="b136f-127">If installed, the item is to be reinstalled in the same state.</span></span> |



 

<span data-ttu-id="b136f-128">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="b136f-128">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b136f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b136f-129">Requirements</span></span>



| <span data-ttu-id="b136f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b136f-130">Requirement</span></span> | <span data-ttu-id="b136f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b136f-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b136f-132">Versão</span><span class="sxs-lookup"><span data-stu-id="b136f-132">Version</span></span><br/> | <span data-ttu-id="b136f-133">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b136f-133">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b136f-134">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b136f-134">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b136f-135">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="b136f-135">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b136f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b136f-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="b136f-137"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b136f-137"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b136f-138">IID</span><span class="sxs-lookup"><span data-stu-id="b136f-138">IID</span></span><br/>     | <span data-ttu-id="b136f-139">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b136f-139">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




