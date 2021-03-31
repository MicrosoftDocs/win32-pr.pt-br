---
description: 'Saiba mais sobre: estrutura de JET_ERRINFOBASIC_W'
title: Estrutura de JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103930774"
---
# <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="9d639-103">Estrutura de JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="9d639-103">JET_ERRINFOBASIC_W Structure</span></span>


<span data-ttu-id="9d639-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9d639-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="9d639-105">Estrutura de JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="9d639-105">JET_ERRINFOBASIC_W Structure</span></span>

<span data-ttu-id="9d639-106">A estrutura de **JET_ERRINFOBASIC_W** define os dados que são retornados do método [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) quando o JET_ErrorInfoSpecificErr InfoLevel é passado.</span><span class="sxs-lookup"><span data-stu-id="9d639-106">The **JET_ERRINFOBASIC_W** structure defines the data that is returned from the [JetGetErrorInfo()](./jetgeterrorinfow-function.md) method when the JET_ErrorInfoSpecificErr InfoLevel is passed in.</span></span>

<span data-ttu-id="9d639-107">Observação: esta documentação se baseia em uma versão preliminar do mecanismo de armazenamento extensível.</span><span class="sxs-lookup"><span data-stu-id="9d639-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="9d639-108">Essas informações estão sujeitas a alterações.</span><span class="sxs-lookup"><span data-stu-id="9d639-108">This information is subject to change.</span></span>

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a><span data-ttu-id="9d639-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9d639-109">Members</span></span>

<span data-ttu-id="9d639-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="9d639-110">**cbStruct**</span></span>

<span data-ttu-id="9d639-111">O tamanho da estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="9d639-111">The size of the structure, in bytes.</span></span> <span data-ttu-id="9d639-112">Ele deve ser definido como sizeof (JET_ERRINFOBASIC).</span><span class="sxs-lookup"><span data-stu-id="9d639-112">It must be set to sizeof( JET_ERRINFOBASIC ).</span></span>

<span data-ttu-id="9d639-113">**errValue**</span><span class="sxs-lookup"><span data-stu-id="9d639-113">**errValue**</span></span>

<span data-ttu-id="9d639-114">O valor de erro que foi avaliado, conforme passado para o argumento *pvResult* para [JetGetErrorInfo ()](./jetgeterrorinfow-function.md).</span><span class="sxs-lookup"><span data-stu-id="9d639-114">The error value that was evaluated, as passed in for the *pvResult* argument to [JetGetErrorInfo()](./jetgeterrorinfow-function.md).</span></span>

<span data-ttu-id="9d639-115">**errcatMostSpecific**</span><span class="sxs-lookup"><span data-stu-id="9d639-115">**errcatMostSpecific**</span></span>

<span data-ttu-id="9d639-116">A constante [JET_ERRCAT](./jet-errcat.md) de nível mais baixo associada ao erro; ou seja, a categoria de nível folha na hierarquia de categoria documentada em [JET_ERRCAT](./jet-errcat.md).</span><span class="sxs-lookup"><span data-stu-id="9d639-116">The lowest-level [JET_ERRCAT](./jet-errcat.md) constant that is associated with the error; that is, the leaf-level category in the category hierarchy documented in [JET_ERRCAT](./jet-errcat.md).</span></span>

<span data-ttu-id="9d639-117">**rgCategoricalHierarchy \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="9d639-117">**rgCategoricalHierarchy\[8\]**</span></span>

<span data-ttu-id="9d639-118">A hierarquia de categorias de erro que está associada ao erro.</span><span class="sxs-lookup"><span data-stu-id="9d639-118">The hierarchy of error categories that is associated with the error.</span></span> <span data-ttu-id="9d639-119">A posição 0 é o nível mais alto na hierarquia de [JET_ERRCAT](./jet-errcat.md)e o restante são subcategorias até que a categoria mais específica seja definida, após a qual todas as categorias são JET_errcatUnknown.</span><span class="sxs-lookup"><span data-stu-id="9d639-119">Position 0 is the highest level in the hierarchy of [JET_ERRCAT](./jet-errcat.md), and the rest are subcategories until the most specific category is set, after which all categories are JET_errcatUnknown.</span></span>

<span data-ttu-id="9d639-120">**lSourceLine**</span><span class="sxs-lookup"><span data-stu-id="9d639-120">**lSourceLine**</span></span>

<span data-ttu-id="9d639-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9d639-121">Reserved.</span></span>

<span data-ttu-id="9d639-122">**rgszSourceFile \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="9d639-122">**rgszSourceFile\[64\]**</span></span>

<span data-ttu-id="9d639-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9d639-123">Reserved.</span></span>

### <a name="requirements"></a><span data-ttu-id="9d639-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d639-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d639-125"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="9d639-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9d639-126">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9d639-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d639-127"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="9d639-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9d639-128">Requer o Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="9d639-128">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d639-129"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="9d639-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9d639-130">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9d639-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
