---
description: 'Saiba mais sobre: método Windows8Api. PrereadKeyRanges'
title: Método Windows8Api. PrereadKeyRanges (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921178"
---
# <a name="windows8apiprereadkeyranges-method"></a><span data-ttu-id="c16bd-103">Método Windows8Api. PrereadKeyRanges</span><span class="sxs-lookup"><span data-stu-id="c16bd-103">Windows8Api.PrereadKeyRanges method</span></span>

<span data-ttu-id="c16bd-104">Se os registros com os intervalos de chave especificados não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c16bd-104">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="c16bd-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c16bd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="c16bd-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c16bd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c16bd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c16bd-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c16bd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c16bd-108">Parameters</span></span>

  - <span data-ttu-id="c16bd-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c16bd-109">sesid</span></span>  
    <span data-ttu-id="c16bd-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c16bd-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c16bd-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c16bd-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-112">TableID</span><span class="sxs-lookup"><span data-stu-id="c16bd-112">tableid</span></span>  
    <span data-ttu-id="c16bd-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c16bd-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c16bd-114">A tabela na qual os itens são relidos.</span><span class="sxs-lookup"><span data-stu-id="c16bd-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-115">keysStart</span><span class="sxs-lookup"><span data-stu-id="c16bd-115">keysStart</span></span>  
    <span data-ttu-id="c16bd-116">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="c16bd-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="c16bd-117">O início dos intervalos de chave para ser lido.</span><span class="sxs-lookup"><span data-stu-id="c16bd-117">The start of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-118">keyStartLengths</span><span class="sxs-lookup"><span data-stu-id="c16bd-118">keyStartLengths</span></span>  
    <span data-ttu-id="c16bd-119">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="c16bd-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="c16bd-120">Os comprimentos das chaves iniciais a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="c16bd-120">The lengths of the start keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-121">Enviar por</span><span class="sxs-lookup"><span data-stu-id="c16bd-121">keysEnd</span></span>  
    <span data-ttu-id="c16bd-122">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="c16bd-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="c16bd-123">O final do intervalo de chaves a ser lido.</span><span class="sxs-lookup"><span data-stu-id="c16bd-123">The end of key rangess to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-124">keyEndLengths</span><span class="sxs-lookup"><span data-stu-id="c16bd-124">keyEndLengths</span></span>  
    <span data-ttu-id="c16bd-125">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="c16bd-125">Type: \[\]</span></span>  
    
    <span data-ttu-id="c16bd-126">Os comprimentos das chaves finais a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="c16bd-126">The lengths of the end keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-127">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="c16bd-127">rangeIndex</span></span>  
    <span data-ttu-id="c16bd-128">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c16bd-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c16bd-129">O índice do primeiro intervalo de chaves na matriz a ser lido.</span><span class="sxs-lookup"><span data-stu-id="c16bd-129">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-130">rangeCount</span><span class="sxs-lookup"><span data-stu-id="c16bd-130">rangeCount</span></span>  
    <span data-ttu-id="c16bd-131">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c16bd-131">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c16bd-132">O número máximo de intervalos de chave a serem lidos.</span><span class="sxs-lookup"><span data-stu-id="c16bd-132">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-133">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="c16bd-133">rangesPreread</span></span>  
    <span data-ttu-id="c16bd-134">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c16bd-134">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c16bd-135">Retorna o número de chaves que realmente são conlidas.</span><span class="sxs-lookup"><span data-stu-id="c16bd-135">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-136">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="c16bd-136">columnsPreread</span></span>  
    <span data-ttu-id="c16bd-137">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="c16bd-137">Type: \[\]</span></span>  
    
    <span data-ttu-id="c16bd-138">Lista de IDs de coluna para colunas de valor longo a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="c16bd-138">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="c16bd-139">grbit</span><span class="sxs-lookup"><span data-stu-id="c16bd-139">grbit</span></span>  
    <span data-ttu-id="c16bd-140">Tipo: [Microsoft. ISAM. ESENT. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c16bd-140">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c16bd-141">Opções de preread.</span><span class="sxs-lookup"><span data-stu-id="c16bd-141">Preread options.</span></span> <span data-ttu-id="c16bd-142">Usado para especificar a direção da subleitura.</span><span class="sxs-lookup"><span data-stu-id="c16bd-142">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="c16bd-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c16bd-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c16bd-144">Referência</span><span class="sxs-lookup"><span data-stu-id="c16bd-144">Reference</span></span>

[<span data-ttu-id="c16bd-145">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c16bd-145">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="c16bd-146">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c16bd-146">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="c16bd-147">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="c16bd-147">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
