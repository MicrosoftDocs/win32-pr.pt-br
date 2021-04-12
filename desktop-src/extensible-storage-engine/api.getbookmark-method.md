---
description: 'Saiba mais sobre: método API. GetBookmark'
title: Método API. GetBookmark
TOCTitle: 'GetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getbookmark(v=EXCHG.10)
ms:contentKeyID: 55100654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edcdfe7ddefadd993ef9c96e6dcc1416080b413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501236"
---
# <a name="apigetbookmark-method"></a><span data-ttu-id="b60d7-103">Método API. GetBookmark</span><span class="sxs-lookup"><span data-stu-id="b60d7-103">Api.GetBookmark method</span></span>

<span data-ttu-id="b60d7-104">Recupera o indicador para o registro que está associado à entrada de índice na posição atual de um cursor.</span><span class="sxs-lookup"><span data-stu-id="b60d7-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="b60d7-105">Esse indicador pode então ser usado para reposicionar esse cursor de volta para o mesmo registro usando JetGotoBookmark.</span><span class="sxs-lookup"><span data-stu-id="b60d7-105">This bookmark can then be used to reposition that cursor back to the same record using JetGotoBookmark.</span></span>

<span data-ttu-id="b60d7-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b60d7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b60d7-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b60d7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b60d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b60d7-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Byte()

returnValue = Api.GetBookmark(sesid, _
    tableid)
```

``` csharp
public static byte[] GetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="b60d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b60d7-109">Parameters</span></span>

  - <span data-ttu-id="b60d7-110">sesid</span><span class="sxs-lookup"><span data-stu-id="b60d7-110">sesid</span></span>  
    <span data-ttu-id="b60d7-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b60d7-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b60d7-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b60d7-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b60d7-113">TableID</span><span class="sxs-lookup"><span data-stu-id="b60d7-113">tableid</span></span>  
    <span data-ttu-id="b60d7-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b60d7-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b60d7-115">O cursor do qual recuperar o indicador.</span><span class="sxs-lookup"><span data-stu-id="b60d7-115">The cursor to retrieve the bookmark from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b60d7-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b60d7-116">Return value</span></span>

<span data-ttu-id="b60d7-117">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="b60d7-117">Type: \[\]</span></span>  
<span data-ttu-id="b60d7-118">O indicador do registro.</span><span class="sxs-lookup"><span data-stu-id="b60d7-118">The bookmark of the record.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b60d7-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b60d7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b60d7-120">Referência</span><span class="sxs-lookup"><span data-stu-id="b60d7-120">Reference</span></span>

[<span data-ttu-id="b60d7-121">Classe de API</span><span class="sxs-lookup"><span data-stu-id="b60d7-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b60d7-122">Membros da API</span><span class="sxs-lookup"><span data-stu-id="b60d7-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b60d7-123">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b60d7-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
