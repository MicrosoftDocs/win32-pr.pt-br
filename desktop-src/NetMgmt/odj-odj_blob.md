---
title: ODJ_BLOB
description: Definição de IDL de ODJ_BLOB
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104454437"
---
# <a name="odj_blob-structure"></a><span data-ttu-id="a3246-103">Estrutura de ODJ_BLOB</span><span class="sxs-lookup"><span data-stu-id="a3246-103">ODJ_BLOB structure</span></span>

<span data-ttu-id="a3246-104">Especifica uma estrutura que contém uma estrutura de ODJ_WIN7BLOB serializada ou uma estrutura de OP_PACKAGE serializada.</span><span class="sxs-lookup"><span data-stu-id="a3246-104">Specifies a structure containing either a serialized ODJ_WIN7BLOB structure or a serialized OP_PACKAGE structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3246-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3246-105">Syntax</span></span>

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a><span data-ttu-id="a3246-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a3246-106">Members</span></span>

### <a name="ulodjformat"></a><span data-ttu-id="a3246-107">ulODJFormat</span><span class="sxs-lookup"><span data-stu-id="a3246-107">ulODJFormat</span></span>

<span data-ttu-id="a3246-108">Especifica a versão lógica da estrutura e deve ser definida como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="a3246-108">Specifies the logical version of the structure and must be set to one of the following values:</span></span>

|<span data-ttu-id="a3246-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a3246-109">Value</span></span>|<span data-ttu-id="a3246-110">Significado</span><span class="sxs-lookup"><span data-stu-id="a3246-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="a3246-111">ODJ_WIN7_FORMAT (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a3246-111">ODJ_WIN7_FORMAT (0x00000001)</span></span>|<span data-ttu-id="a3246-112">Os bytes contidos em pBlob devem conter uma estrutura de ODJ_WIN7_BLOB serializada.</span><span class="sxs-lookup"><span data-stu-id="a3246-112">The bytes contained in pBlob must contain a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="a3246-113">ODJ_WIN8_FORMAT (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a3246-113">ODJ_WIN8_FORMAT (0x00000002)</span></span>|<span data-ttu-id="a3246-114">Os bytes contidos em pBlob devem conter uma estrutura de OP_PACKAGE serializada.</span><span class="sxs-lookup"><span data-stu-id="a3246-114">The bytes contained in pBlob must contain a serialized OP_PACKAGE structure.</span></span>|

### <a name="cbblob"></a><span data-ttu-id="a3246-115">cbBlob</span><span class="sxs-lookup"><span data-stu-id="a3246-115">cbBlob</span></span>

<span data-ttu-id="a3246-116">Isso deve ser definido como o número de bytes na matriz pBlob.</span><span class="sxs-lookup"><span data-stu-id="a3246-116">This must be set to the number of bytes in the pBlob array.</span></span>

### <a name="pblob"></a><span data-ttu-id="a3246-117">pBlob</span><span class="sxs-lookup"><span data-stu-id="a3246-117">pBlob</span></span>

<span data-ttu-id="a3246-118">Aponta para um buffer de bytes que contém uma estrutura serializada, conforme especificado por ulODJFormat acima.</span><span class="sxs-lookup"><span data-stu-id="a3246-118">Points to a byte buffer containing a serialized structure as specified by ulODJFormat above.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3246-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3246-119">See also</span></span>

[<span data-ttu-id="a3246-120">**Definições de IDL de ingresso no domínio offline**</span><span class="sxs-lookup"><span data-stu-id="a3246-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

