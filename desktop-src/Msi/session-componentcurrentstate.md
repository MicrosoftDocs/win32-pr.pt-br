---
description: A propriedade ComponentCurrentState do objeto Session é uma propriedade somente leitura que retorna o estado atual instalado do componente designado. Para valores de estado, consulte a propriedade ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Propriedade Session. ComponentCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c556dd9656ebced155ef90fe96abd394a32ff1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747737"
---
# <a name="sessioncomponentcurrentstate-property"></a><span data-ttu-id="e8c4b-104">Propriedade Session. ComponentCurrentState</span><span class="sxs-lookup"><span data-stu-id="e8c4b-104">Session.ComponentCurrentState property</span></span>

<span data-ttu-id="e8c4b-105">A propriedade **ComponentCurrentState** do objeto [**Session**](session-object.md) é uma propriedade somente leitura que retorna o estado atual instalado do componente designado.</span><span class="sxs-lookup"><span data-stu-id="e8c4b-105">The **ComponentCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated component.</span></span> <span data-ttu-id="e8c4b-106">Para valores de estado, consulte a propriedade [**ComponentRequestState**](session-componentrequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="e8c4b-106">For state values, see the [**ComponentRequestState**](session-componentrequeststate.md) property.</span></span>

<span data-ttu-id="e8c4b-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e8c4b-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c4b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8c4b-108">Syntax</span></span>


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a><span data-ttu-id="e8c4b-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e8c4b-109">Property value</span></span>

<span data-ttu-id="e8c4b-110">Nome de cadeia de caracteres necessário do componente solicitado, chave primária na tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="e8c4b-110">Required string name of the requested component, primary key into the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c4b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8c4b-111">Remarks</span></span>

<span data-ttu-id="e8c4b-112">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="e8c4b-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c4b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8c4b-113">Requirements</span></span>



| <span data-ttu-id="e8c4b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c4b-114">Requirement</span></span> | <span data-ttu-id="e8c4b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e8c4b-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c4b-116">Versão</span><span class="sxs-lookup"><span data-stu-id="e8c4b-116">Version</span></span><br/> | <span data-ttu-id="e8c4b-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e8c4b-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e8c4b-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e8c4b-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e8c4b-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e8c4b-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e8c4b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e8c4b-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="e8c4b-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8c4b-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e8c4b-122">IID</span><span class="sxs-lookup"><span data-stu-id="e8c4b-122">IID</span></span><br/>     | <span data-ttu-id="e8c4b-123">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e8c4b-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="e8c4b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8c4b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c4b-125">**Session**</span><span class="sxs-lookup"><span data-stu-id="e8c4b-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="e8c4b-126">**Propriedade ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="e8c4b-126">**ComponentRequestState property**</span></span>](session-componentrequeststate.md)
</dt> </dl>

 

 




