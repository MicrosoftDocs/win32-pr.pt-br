---
description: O método FETCH do objeto View recupera a próxima linha de dados da coluna se houver mais linhas disponíveis no conjunto de resultados; caso contrário, será NULL. Chame o método execute antes do método Fetch.
ms.assetid: d51bf60d-5725-41eb-9002-1d0e5b9f50a3
title: Método View. Fetch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Fetch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f16d3a14f3c4f54f64364488322007a99c0f7cd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758609"
---
# <a name="viewfetch-method"></a><span data-ttu-id="3331e-104">Método View. Fetch</span><span class="sxs-lookup"><span data-stu-id="3331e-104">View.Fetch method</span></span>

<span data-ttu-id="3331e-105">O método **Fetch** do objeto [**View**](view-object.md) recupera a próxima linha de dados da coluna se houver mais linhas disponíveis no conjunto de resultados; caso contrário, será NULL.</span><span class="sxs-lookup"><span data-stu-id="3331e-105">The **Fetch** method of the [**View**](view-object.md) object retrieves the next row of column data if more rows are available in the result set, otherwise it is Null.</span></span> <span data-ttu-id="3331e-106">Chame o método [**Execute**](view-execute.md) antes do método **Fetch** .</span><span class="sxs-lookup"><span data-stu-id="3331e-106">Call the [**Execute**](view-execute.md) method before the **Fetch** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3331e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3331e-107">Syntax</span></span>


```JScript
View.Fetch()
```



## <a name="parameters"></a><span data-ttu-id="3331e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3331e-108">Parameters</span></span>

<span data-ttu-id="3331e-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3331e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3331e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3331e-110">Return value</span></span>

<span data-ttu-id="3331e-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3331e-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3331e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3331e-112">Remarks</span></span>

<span data-ttu-id="3331e-113">O mesmo objeto de [**registro**](record-object.md) deve ser usado para recuperar os dados em várias linhas, caso contrário, o objeto deve ser liberado saindo do escopo.</span><span class="sxs-lookup"><span data-stu-id="3331e-113">The same [**Record**](record-object.md) object should be used to retrieve the data in multiple rows, or else the object should be released by going out of scope.</span></span> <span data-ttu-id="3331e-114">O registro pode ser testado para o final do conjunto de resultados usando a sintaxe "If FetchRecord Is Nothing".</span><span class="sxs-lookup"><span data-stu-id="3331e-114">The record can be tested for the end of the result set using the syntax "If FetchRecord Is Nothing".</span></span>

## <a name="requirements"></a><span data-ttu-id="3331e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3331e-115">Requirements</span></span>



| <span data-ttu-id="3331e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3331e-116">Requirement</span></span> | <span data-ttu-id="3331e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3331e-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3331e-118">Versão</span><span class="sxs-lookup"><span data-stu-id="3331e-118">Version</span></span><br/> | <span data-ttu-id="3331e-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3331e-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3331e-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3331e-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3331e-121">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="3331e-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3331e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3331e-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="3331e-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3331e-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3331e-124">IID</span><span class="sxs-lookup"><span data-stu-id="3331e-124">IID</span></span><br/>     | <span data-ttu-id="3331e-125">IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3331e-125">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




