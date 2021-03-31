---
description: 'Saiba mais sobre: método API. RetrieveKey'
title: Método API. RetrieveKey
TOCTitle: 'RetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievekey(v=EXCHG.10)
ms:contentKeyID: 55100880
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fcabab7639a9cf3128b0b2c314ba60c2de8f8e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646647"
---
# <a name="apiretrievekey-method"></a><span data-ttu-id="b9dfa-103">Método API. RetrieveKey</span><span class="sxs-lookup"><span data-stu-id="b9dfa-103">Api.RetrieveKey method</span></span>

<span data-ttu-id="b9dfa-104">Recupera a chave da entrada de índice na posição atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="b9dfa-104">Retrieves the key for the index entry at the current position of a cursor.</span></span>

<span data-ttu-id="b9dfa-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9dfa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9dfa-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b9dfa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9dfa-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9dfa-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As RetrieveKeyGrbit _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As RetrieveKeyGrbit
Dim returnValue As Byte()

returnValue = Api.RetrieveKey(sesid, _
    tableid, grbit)
```

``` csharp
public static byte[] RetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b9dfa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9dfa-108">Parameters</span></span>

  - <span data-ttu-id="b9dfa-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b9dfa-109">sesid</span></span>  
    <span data-ttu-id="b9dfa-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9dfa-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b9dfa-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b9dfa-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9dfa-112">TableID</span><span class="sxs-lookup"><span data-stu-id="b9dfa-112">tableid</span></span>  
    <span data-ttu-id="b9dfa-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9dfa-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b9dfa-114">O cursor do qual recuperar a chave.</span><span class="sxs-lookup"><span data-stu-id="b9dfa-114">The cursor to retrieve the key from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b9dfa-115">grbit</span><span class="sxs-lookup"><span data-stu-id="b9dfa-115">grbit</span></span>  
    <span data-ttu-id="b9dfa-116">Tipo: [Microsoft. ISAM. ESENT. Interop. RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b9dfa-116">Type: [Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit](./retrievekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b9dfa-117">Recuperar opções de chave.</span><span class="sxs-lookup"><span data-stu-id="b9dfa-117">Retrieve key options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b9dfa-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9dfa-118">Return value</span></span>

<span data-ttu-id="b9dfa-119">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="b9dfa-119">Type: \[\]</span></span>  
<span data-ttu-id="b9dfa-120">A chave recuperada.</span><span class="sxs-lookup"><span data-stu-id="b9dfa-120">The retrieved key.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9dfa-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9dfa-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9dfa-122">Referência</span><span class="sxs-lookup"><span data-stu-id="b9dfa-122">Reference</span></span>

[<span data-ttu-id="b9dfa-123">Classe de API</span><span class="sxs-lookup"><span data-stu-id="b9dfa-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b9dfa-124">Membros da API</span><span class="sxs-lookup"><span data-stu-id="b9dfa-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b9dfa-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b9dfa-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
