---
description: A propriedade DVDUniqueID recupera um número gerado pelo sistema que identifica exclusivamente o disco atual.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Propriedade DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825792"
---
# <a name="dvduniqueid-property"></a><span data-ttu-id="e9269-103">Propriedade DVDUniqueID</span><span class="sxs-lookup"><span data-stu-id="e9269-103">DVDUniqueID Property</span></span>

> [!Note]  
> <span data-ttu-id="e9269-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9269-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e9269-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e9269-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e9269-106">A `DVDUniqueID` propriedade recupera um número gerado pelo sistema que identifica exclusivamente o disco atual.</span><span class="sxs-lookup"><span data-stu-id="e9269-106">The `DVDUniqueID` property retrieves a system-generated number that uniquely identifies the current disc.</span></span>

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a><span data-ttu-id="e9269-107">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e9269-107">Return Value</span></span>

<span data-ttu-id="e9269-108">Retorna um valor inteiro que identifica exclusivamente o disco atual.</span><span class="sxs-lookup"><span data-stu-id="e9269-108">Returns an integer value that uniquely identifies the current disc.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9269-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9269-109">Remarks</span></span>

<span data-ttu-id="e9269-110">Esta propriedade é somente leitura sem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="e9269-110">This property is read-only with no default value.</span></span> <span data-ttu-id="e9269-111">O número do identificador (ID) não é absolutamente exclusivo, mas é exclusivo para todas as finalidades práticas.</span><span class="sxs-lookup"><span data-stu-id="e9269-111">The identifier (ID) number is not absolutely unique, but it is unique for all practical purposes.</span></span> <span data-ttu-id="e9269-112">A ID se aplica a todas as cópias replicadas de um disco. Em outras palavras, todas as cópias de um filme específico têm a mesma ID.</span><span class="sxs-lookup"><span data-stu-id="e9269-112">The ID applies to all replicated copies of a disc. In other words, all copies of a specific movie have the same ID.</span></span> <span data-ttu-id="e9269-113">A ID é baseada em tamanhos de arquivo, datas e outras informações, e não no valor BCA.</span><span class="sxs-lookup"><span data-stu-id="e9269-113">The ID is based on file sizes, dates, and other information, and not the BCA value.</span></span>

 

 



