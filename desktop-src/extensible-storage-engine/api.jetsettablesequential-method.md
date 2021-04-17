---
description: 'Saiba mais sobre: método API. JetSetTableSequential'
title: Método API. JetSetTableSequential
TOCTitle: 'JetSetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 879eca53c4867bb41ee0a231bff9adce39aa58a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787646"
---
# <a name="apijetsettablesequential-method"></a><span data-ttu-id="44e37-103">Método API. JetSetTableSequential</span><span class="sxs-lookup"><span data-stu-id="44e37-103">Api.JetSetTableSequential method</span></span>

<span data-ttu-id="44e37-104">Notifica o mecanismo de banco de dados de que o aplicativo está verificando o índice inteiro no qual o cursor está posicionado.</span><span class="sxs-lookup"><span data-stu-id="44e37-104">Notifies the database engine that the application is scanning the entire index that the cursor is positioned on.</span></span> <span data-ttu-id="44e37-105">Consequentemente, os métodos usados para acessar os dados do índice serão ajustados para tornar esse cenário o mais rápido possível.</span><span class="sxs-lookup"><span data-stu-id="44e37-105">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span> <span data-ttu-id="44e37-106">Consulte também [JetResetTableSequential (JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="44e37-106">Also see [JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span></span>

<span data-ttu-id="44e37-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44e37-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44e37-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44e37-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44e37-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44e37-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetTableSequentialGrbitApi.JetSetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetSetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="44e37-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44e37-110">Parameters</span></span>

  - <span data-ttu-id="44e37-111">sesid</span><span class="sxs-lookup"><span data-stu-id="44e37-111">sesid</span></span>  
    <span data-ttu-id="44e37-112">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44e37-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="44e37-113">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="44e37-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="44e37-114">TableID</span><span class="sxs-lookup"><span data-stu-id="44e37-114">tableid</span></span>  
    <span data-ttu-id="44e37-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44e37-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="44e37-116">O cursor que acessará os dados.</span><span class="sxs-lookup"><span data-stu-id="44e37-116">The cursor that will be accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="44e37-117">grbit</span><span class="sxs-lookup"><span data-stu-id="44e37-117">grbit</span></span>  
    <span data-ttu-id="44e37-118">Tipo: [Microsoft. ISAM. ESENT. Interop. SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="44e37-118">Type: [Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="44e37-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="44e37-119">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="44e37-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="44e37-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44e37-121">Referência</span><span class="sxs-lookup"><span data-stu-id="44e37-121">Reference</span></span>

[<span data-ttu-id="44e37-122">Classe de API</span><span class="sxs-lookup"><span data-stu-id="44e37-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="44e37-123">Membros da API</span><span class="sxs-lookup"><span data-stu-id="44e37-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="44e37-124">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="44e37-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
