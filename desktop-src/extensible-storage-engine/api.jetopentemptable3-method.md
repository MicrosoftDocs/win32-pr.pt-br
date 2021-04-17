---
description: 'Saiba mais sobre: método API. JetOpenTempTable3'
title: Método Api.JetOpenTempTable3
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764000"
---
# <a name="apijetopentemptable3-method"></a><span data-ttu-id="55106-103">Método Api.JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="55106-103">Api.JetOpenTempTable3 method</span></span>

<span data-ttu-id="55106-104">Cria uma tabela temporária com um único índice.</span><span class="sxs-lookup"><span data-stu-id="55106-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="55106-105">Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="55106-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="55106-106">No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil.</span><span class="sxs-lookup"><span data-stu-id="55106-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="55106-107">Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial.</span><span class="sxs-lookup"><span data-stu-id="55106-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="55106-108">Consulte também [JetOpenTempTable (JET_SESID, \[ \] Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="55106-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="55106-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55106-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55106-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55106-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55106-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55106-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="55106-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55106-112">Parameters</span></span>

  - <span data-ttu-id="55106-113">sesid</span><span class="sxs-lookup"><span data-stu-id="55106-113">sesid</span></span>  
    <span data-ttu-id="55106-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="55106-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="55106-115">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="55106-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="55106-116">colunas</span><span class="sxs-lookup"><span data-stu-id="55106-116">columns</span></span>  
    <span data-ttu-id="55106-117">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="55106-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="55106-118">Definições de coluna para as colunas criadas na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="55106-118">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="55106-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="55106-119">numColumns</span></span>  
    <span data-ttu-id="55106-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="55106-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="55106-121">Número de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="55106-121">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="55106-122">unicodeindex</span><span class="sxs-lookup"><span data-stu-id="55106-122">unicodeindex</span></span>  
    <span data-ttu-id="55106-123">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="55106-123">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  
    
    <span data-ttu-id="55106-124">Os sinalizadores de ID de localidade e normalização que serão usados para comparar quaisquer dados de coluna de chave Unicode na tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="55106-124">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="55106-125">Quando não estiver presente, as opções padrão serão usadas.</span><span class="sxs-lookup"><span data-stu-id="55106-125">When this is not present then the default options are used.</span></span>

<!-- end list -->

  - <span data-ttu-id="55106-126">grbit</span><span class="sxs-lookup"><span data-stu-id="55106-126">grbit</span></span>  
    <span data-ttu-id="55106-127">Tipo: [Microsoft. ISAM. ESENT. Interop. TempTableGrbit](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="55106-127">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="55106-128">Opções de criação de tabela.</span><span class="sxs-lookup"><span data-stu-id="55106-128">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="55106-129">TableID</span><span class="sxs-lookup"><span data-stu-id="55106-129">tableid</span></span>  
    <span data-ttu-id="55106-130">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="55106-130">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="55106-131">Retorna a TableName da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="55106-131">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="55106-132">Fechar este TableName com [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) libera os recursos associados à tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="55106-132">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="55106-133">columnids</span><span class="sxs-lookup"><span data-stu-id="55106-133">columnids</span></span>  
    <span data-ttu-id="55106-134">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="55106-134">Type: \[\]</span></span>  
    
    <span data-ttu-id="55106-135">O buffer de saída que recebe a matriz de IDs de coluna geradas durante a criação da tabela temporária.</span><span class="sxs-lookup"><span data-stu-id="55106-135">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="55106-136">As IDs de coluna nessa matriz correspondem exatamente à matriz de entrada de definições de coluna.</span><span class="sxs-lookup"><span data-stu-id="55106-136">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="55106-137">Como resultado, o tamanho desse buffer deve corresponder ao tamanho da matriz de entrada.</span><span class="sxs-lookup"><span data-stu-id="55106-137">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="55106-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="55106-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55106-139">Referência</span><span class="sxs-lookup"><span data-stu-id="55106-139">Reference</span></span>

[<span data-ttu-id="55106-140">Classe de API</span><span class="sxs-lookup"><span data-stu-id="55106-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="55106-141">Membros da API</span><span class="sxs-lookup"><span data-stu-id="55106-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="55106-142">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="55106-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
