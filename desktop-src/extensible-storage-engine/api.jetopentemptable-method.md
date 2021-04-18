---
description: 'Saiba mais sobre: método API. JetOpenTempTable'
title: Método API. JetOpenTempTable
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa41ce62b8bc2d7f2429acb5de809ad0be44a609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810643"
---
# <a name="apijetopentemptable-method"></a><span data-ttu-id="98719-103">Método API. JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="98719-103">Api.JetOpenTempTable method</span></span>

<span data-ttu-id="98719-104">Cria uma tabela temporária com um único índice.</span><span class="sxs-lookup"><span data-stu-id="98719-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="98719-105">Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="98719-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="98719-106">No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil.</span><span class="sxs-lookup"><span data-stu-id="98719-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="98719-107">Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial.</span><span class="sxs-lookup"><span data-stu-id="98719-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="98719-108">Consulte também [JetOpenTempTable3 (JET_SESID, \[ \] Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="98719-108">Also see [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="98719-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="98719-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="98719-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="98719-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="98719-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="98719-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="98719-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98719-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="98719-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98719-113">Parameters</span></span>

  - <span data-ttu-id="98719-114">sesid</span><span class="sxs-lookup"><span data-stu-id="98719-114">sesid</span></span>  
    <span data-ttu-id="98719-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="98719-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="98719-116">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="98719-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="98719-117">colunas</span><span class="sxs-lookup"><span data-stu-id="98719-117">columns</span></span>  
    <span data-ttu-id="98719-118">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="98719-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="98719-119">Definições de coluna para as colunas criadas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="98719-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="98719-120">numColumns</span><span class="sxs-lookup"><span data-stu-id="98719-120">numColumns</span></span>  
    <span data-ttu-id="98719-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="98719-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="98719-122">Número de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="98719-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="98719-123">grbit</span><span class="sxs-lookup"><span data-stu-id="98719-123">grbit</span></span>  
    <span data-ttu-id="98719-124">Tipo: [Microsoft. ISAM. ESENT. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="98719-124">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="98719-125">Opções de criação de tabela.</span><span class="sxs-lookup"><span data-stu-id="98719-125">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="98719-126">TableID</span><span class="sxs-lookup"><span data-stu-id="98719-126">tableid</span></span>  
    <span data-ttu-id="98719-127">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="98719-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="98719-128">Retorna a TableName da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="98719-128">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="98719-129">Fechar este TableName com [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libera os recursos associados à tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="98719-129">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="98719-130">columnids</span><span class="sxs-lookup"><span data-stu-id="98719-130">columnids</span></span>  
    <span data-ttu-id="98719-131">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="98719-131">Type: \[\]</span></span>  
    
    <span data-ttu-id="98719-132">O buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="98719-132">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="98719-133">As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="98719-133">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="98719-134">Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="98719-134">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="98719-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="98719-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="98719-136">Referência</span><span class="sxs-lookup"><span data-stu-id="98719-136">Reference</span></span>

[<span data-ttu-id="98719-137">Classe de API</span><span class="sxs-lookup"><span data-stu-id="98719-137">Api class</span></span>](./api-class.md)

[<span data-ttu-id="98719-138">Membros da API</span><span class="sxs-lookup"><span data-stu-id="98719-138">Api members</span></span>](./api-members.md)

[<span data-ttu-id="98719-139">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="98719-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
