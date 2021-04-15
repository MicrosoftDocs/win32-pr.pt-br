---
description: A propriedade DataSize do objeto Record é uma propriedade somente leitura que retorna o tamanho dos dados para o campo designado.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Propriedade Record. DataSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747324"
---
# <a name="recorddatasize-property"></a><span data-ttu-id="c23de-103">Propriedade Record. DataSize</span><span class="sxs-lookup"><span data-stu-id="c23de-103">Record.DataSize property</span></span>

<span data-ttu-id="c23de-104">A propriedade **DataSize** do objeto [**Record**](record-object.md) é uma propriedade somente leitura que retorna o tamanho dos dados para o campo designado.</span><span class="sxs-lookup"><span data-stu-id="c23de-104">The **DataSize** property of the [**Record**](record-object.md) object is a read-only property that returns the size of the data for the designated field.</span></span> <span data-ttu-id="c23de-105">Se os dados forem um fluxo, o tamanho do fluxo em bytes será retornado.</span><span class="sxs-lookup"><span data-stu-id="c23de-105">If the data is a stream, the stream length in bytes is returned.</span></span> <span data-ttu-id="c23de-106">Se os dados forem uma cadeia de caracteres, o comprimento da cadeia de caracteres sem NULL será retornado.</span><span class="sxs-lookup"><span data-stu-id="c23de-106">If the data is a string, the string length without Null is returned.</span></span> <span data-ttu-id="c23de-107">Se os dados forem um inteiro, o valor 4 será retornado (indicando o tamanho do inteiro).</span><span class="sxs-lookup"><span data-stu-id="c23de-107">If the data is an integer, the value 4 is returned (indicating the size of the integer).</span></span> <span data-ttu-id="c23de-108">Se os dados forem nulos, 0 será retornado.</span><span class="sxs-lookup"><span data-stu-id="c23de-108">If the data is Null, 0 is returned.</span></span>

<span data-ttu-id="c23de-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c23de-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c23de-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c23de-110">Syntax</span></span>


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a><span data-ttu-id="c23de-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c23de-111">Property value</span></span>

<span data-ttu-id="c23de-112">Campo obrigatório número do valor dentro do registro, baseado em 1.</span><span class="sxs-lookup"><span data-stu-id="c23de-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="c23de-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c23de-113">Requirements</span></span>



| <span data-ttu-id="c23de-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c23de-114">Requirement</span></span> | <span data-ttu-id="c23de-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c23de-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c23de-116">Versão</span><span class="sxs-lookup"><span data-stu-id="c23de-116">Version</span></span><br/> | <span data-ttu-id="c23de-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c23de-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c23de-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c23de-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c23de-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c23de-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c23de-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c23de-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c23de-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c23de-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c23de-122">IID</span><span class="sxs-lookup"><span data-stu-id="c23de-122">IID</span></span><br/>     | <span data-ttu-id="c23de-123">IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c23de-123">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




