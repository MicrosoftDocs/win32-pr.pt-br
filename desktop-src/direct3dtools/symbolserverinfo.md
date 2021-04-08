---
description: Representa informações sobre o servidor de símbolo de depuração.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura SymbolServerInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087484"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span data-ttu-id="b0ef5-103"><span id="vspixengine.symbolserverinfo"></span>Estrutura SymbolServerInfo</span><span class="sxs-lookup"><span data-stu-id="b0ef5-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo structure</span></span>

<span data-ttu-id="b0ef5-104">Representa informações sobre o servidor de símbolo de depuração.</span><span class="sxs-lookup"><span data-stu-id="b0ef5-104">Represents information about the debug symbol server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ef5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0ef5-105">Syntax</span></span>


```C++
} SymbolServerInfo;
```

## <a name="members"></a><span data-ttu-id="b0ef5-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b0ef5-106">Members</span></span>

<span data-ttu-id="b0ef5-107">**symbolPath**</span><span class="sxs-lookup"><span data-stu-id="b0ef5-107">**symbolPath**</span></span>  
<span data-ttu-id="b0ef5-108">Uma cadeia de caracteres COM que contém o caminho do servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="b0ef5-108">A COM string containing the path of the symbol server.</span></span>

<span data-ttu-id="b0ef5-109">**symbolCacheDir**</span><span class="sxs-lookup"><span data-stu-id="b0ef5-109">**symbolCacheDir**</span></span>  
<span data-ttu-id="b0ef5-110">Uma cadeia de caracteres COM que contém o diretório de cache do servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="b0ef5-110">A COM string containing the cache directory of the symbol server.</span></span>

<span data-ttu-id="b0ef5-111">**publicSymbolServerName**</span><span class="sxs-lookup"><span data-stu-id="b0ef5-111">**publicSymbolServerName**</span></span>  
<span data-ttu-id="b0ef5-112">Uma cadeia de caracteres COM que contém o nome público do servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="b0ef5-112">A COM string containing the public name of the symbol server.</span></span>

<span data-ttu-id="b0ef5-113">**symbolExcludeList**</span><span class="sxs-lookup"><span data-stu-id="b0ef5-113">**symbolExcludeList**</span></span>  
<span data-ttu-id="b0ef5-114">Uma cadeia de caracteres COM que especifica a lista de símbolos a serem excluídos.</span><span class="sxs-lookup"><span data-stu-id="b0ef5-114">A COM string that specifies the list of symbols to exclude.</span></span>

<span data-ttu-id="b0ef5-115">**symbolIncludeList**</span><span class="sxs-lookup"><span data-stu-id="b0ef5-115">**symbolIncludeList**</span></span>  
<span data-ttu-id="b0ef5-116">Uma cadeia de caracteres COM que especifica a lista de símbolos a serem incluídos.</span><span class="sxs-lookup"><span data-stu-id="b0ef5-116">A COM string that specifies the list of symbols to include.</span></span>

<span data-ttu-id="b0ef5-117">**useExcludeList**</span><span class="sxs-lookup"><span data-stu-id="b0ef5-117">**useExcludeList**</span></span>  
<span data-ttu-id="b0ef5-118">true se a lista de exclusões for ignorada; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="b0ef5-118">true if the exclude list is ignored; otherwise, false.</span></span>

<span data-ttu-id="b0ef5-119">**useMSSymbolServer**</span><span class="sxs-lookup"><span data-stu-id="b0ef5-119">**useMSSymbolServer**</span></span>  
<span data-ttu-id="b0ef5-120">true se estiver usando o Microsoft Symbol Server; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="b0ef5-120">true if using Microsoft symbol server; otherwise, false.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0ef5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0ef5-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b0ef5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0ef5-122">Header</span></span></p></td><td><span data-ttu-id="b0ef5-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b0ef5-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



