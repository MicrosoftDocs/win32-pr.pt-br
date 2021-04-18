---
description: O método Persist do objeto SummaryInfo formata e grava as propriedades armazenadas anteriormente no fluxo SummaryInformation padrão.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: Método SummaryInfo. Persist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810314"
---
# <a name="summaryinfopersist-method"></a><span data-ttu-id="723d7-103">Método SummaryInfo. Persist</span><span class="sxs-lookup"><span data-stu-id="723d7-103">SummaryInfo.Persist method</span></span>

<span data-ttu-id="723d7-104">O método **Persist** do objeto [**SummaryInfo**](summaryinfo-object.md) formata e grava as propriedades armazenadas anteriormente no fluxo SummaryInformation padrão.</span><span class="sxs-lookup"><span data-stu-id="723d7-104">The **Persist** method of the [**SummaryInfo**](summaryinfo-object.md) object formats and writes the previously stored properties into the standard SummaryInformation stream.</span></span> <span data-ttu-id="723d7-105">Ele gera um erro se o fluxo não puder ser gravado com êxito.</span><span class="sxs-lookup"><span data-stu-id="723d7-105">It generates an error if the stream cannot be successfully written.</span></span> <span data-ttu-id="723d7-106">Esse método só pode ser chamado uma vez depois que todos os valores de propriedade tiverem sido definidos.</span><span class="sxs-lookup"><span data-stu-id="723d7-106">This method may only be called once after all the property values have been set.</span></span> <span data-ttu-id="723d7-107">As propriedades ainda podem ser lidas depois que o fluxo é gravado.</span><span class="sxs-lookup"><span data-stu-id="723d7-107">Properties may still be read after the stream is written.</span></span>

## <a name="syntax"></a><span data-ttu-id="723d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="723d7-108">Syntax</span></span>


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a><span data-ttu-id="723d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="723d7-109">Parameters</span></span>

<span data-ttu-id="723d7-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="723d7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="723d7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="723d7-111">Return value</span></span>

<span data-ttu-id="723d7-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="723d7-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="723d7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="723d7-113">Requirements</span></span>



| <span data-ttu-id="723d7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="723d7-114">Requirement</span></span> | <span data-ttu-id="723d7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="723d7-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723d7-116">Versão</span><span class="sxs-lookup"><span data-stu-id="723d7-116">Version</span></span><br/> | <span data-ttu-id="723d7-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="723d7-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="723d7-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="723d7-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="723d7-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="723d7-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="723d7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="723d7-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="723d7-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="723d7-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="723d7-122">IID</span><span class="sxs-lookup"><span data-stu-id="723d7-122">IID</span></span><br/>     | <span data-ttu-id="723d7-123">IID \_ ISummaryInfo é definido como 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="723d7-123">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



 

 




