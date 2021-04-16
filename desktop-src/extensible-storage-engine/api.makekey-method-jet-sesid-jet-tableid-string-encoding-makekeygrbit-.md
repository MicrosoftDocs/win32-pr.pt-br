---
description: 'Saiba mais sobre: método API. MakeKey (JET_SESID, JET_TABLEID, Cadeia de caracteres, codificação, MakeKeyGrbit)'
title: Método API. MakeKey (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.Text.Encoding,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100830
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5f4fa9dfd848ff6aef858533501891e08ef8972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782447"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-string-encoding-makekeygrbit"></a><span data-ttu-id="32eed-103">Método API. MakeKey (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="32eed-103">Api.MakeKey method (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)</span></span>

<span data-ttu-id="32eed-104">Constrói uma chave de pesquisa que pode ser usada por [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="32eed-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="32eed-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="32eed-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="32eed-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="32eed-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="32eed-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32eed-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As String, _
    encoding As Encoding, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As String
Dim encoding As Encoding
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    encoding, grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string data,
    Encoding encoding,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="32eed-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32eed-108">Parameters</span></span>

  - <span data-ttu-id="32eed-109">sesid</span><span class="sxs-lookup"><span data-stu-id="32eed-109">sesid</span></span>  
    <span data-ttu-id="32eed-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="32eed-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="32eed-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="32eed-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="32eed-112">TableID</span><span class="sxs-lookup"><span data-stu-id="32eed-112">tableid</span></span>  
    <span data-ttu-id="32eed-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="32eed-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="32eed-114">O cursor no qual criar a chave.</span><span class="sxs-lookup"><span data-stu-id="32eed-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="32eed-115">data</span><span class="sxs-lookup"><span data-stu-id="32eed-115">data</span></span>  
    <span data-ttu-id="32eed-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="32eed-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="32eed-117">Dados da coluna para a coluna de chave atual do índice atual.</span><span class="sxs-lookup"><span data-stu-id="32eed-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="32eed-118">codificando</span><span class="sxs-lookup"><span data-stu-id="32eed-118">encoding</span></span>  
    <span data-ttu-id="32eed-119">Tipo: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="32eed-119">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="32eed-120">A codificação usada para converter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="32eed-120">The encoding used to convert the string.</span></span>

<!-- end list -->

  - <span data-ttu-id="32eed-121">grbit</span><span class="sxs-lookup"><span data-stu-id="32eed-121">grbit</span></span>  
    <span data-ttu-id="32eed-122">Tipo: [Microsoft. ISAM. ESENT. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="32eed-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="32eed-123">Opções de chave.</span><span class="sxs-lookup"><span data-stu-id="32eed-123">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="32eed-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="32eed-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="32eed-125">Referência</span><span class="sxs-lookup"><span data-stu-id="32eed-125">Reference</span></span>

[<span data-ttu-id="32eed-126">Classe de API</span><span class="sxs-lookup"><span data-stu-id="32eed-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="32eed-127">Membros da API</span><span class="sxs-lookup"><span data-stu-id="32eed-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="32eed-128">Sobrecarga de MakeKey</span><span class="sxs-lookup"><span data-stu-id="32eed-128">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="32eed-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="32eed-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
