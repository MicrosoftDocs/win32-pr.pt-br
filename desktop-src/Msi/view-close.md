---
description: O método Close do objeto View encerra a execução da consulta e libera os recursos do banco de dados.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: Método View. Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770168"
---
# <a name="viewclose-method"></a><span data-ttu-id="87ec9-103">Método View. Close</span><span class="sxs-lookup"><span data-stu-id="87ec9-103">View.Close method</span></span>

<span data-ttu-id="87ec9-104">O método **Close** do objeto [**View**](view-object.md) encerra a execução da consulta e libera os recursos do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87ec9-104">The **Close** method of the [**View**](view-object.md) object terminates query execution and releases database resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="87ec9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87ec9-105">Syntax</span></span>


```JScript
View.Close()
```



## <a name="parameters"></a><span data-ttu-id="87ec9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87ec9-106">Parameters</span></span>

<span data-ttu-id="87ec9-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="87ec9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87ec9-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87ec9-108">Return value</span></span>

<span data-ttu-id="87ec9-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="87ec9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87ec9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="87ec9-110">Remarks</span></span>

<span data-ttu-id="87ec9-111">Esse método deve ser chamado antes que o método [**Execute**](view-execute.md) seja chamado novamente no objeto [**View**](view-object.md) , a menos que todas as linhas do conjunto de resultados tenham sido obtidas com o método [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="87ec9-111">This method must be called before the [**Execute**](view-execute.md) method is called again on the [**View**](view-object.md) object unless all rows of the result set have been obtained with the [**Fetch**](view-fetch.md) method.</span></span> <span data-ttu-id="87ec9-112">Ele é chamado internamente quando a exibição é destruída.</span><span class="sxs-lookup"><span data-stu-id="87ec9-112">It is called internally when the view is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ec9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87ec9-113">Requirements</span></span>



| <span data-ttu-id="87ec9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="87ec9-114">Requirement</span></span> | <span data-ttu-id="87ec9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="87ec9-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ec9-116">Versão</span><span class="sxs-lookup"><span data-stu-id="87ec9-116">Version</span></span><br/> | <span data-ttu-id="87ec9-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="87ec9-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="87ec9-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="87ec9-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="87ec9-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="87ec9-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="87ec9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="87ec9-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="87ec9-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87ec9-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="87ec9-122">IID</span><span class="sxs-lookup"><span data-stu-id="87ec9-122">IID</span></span><br/>     | <span data-ttu-id="87ec9-123">IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="87ec9-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




