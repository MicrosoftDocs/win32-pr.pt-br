---
description: 'Saiba mais sobre: método Windows8Api. JetOpenTemporaryTable2'
title: Método Windows8Api. JetOpenTemporaryTable2 (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetOpenTemporaryTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetopentemporarytable2(v=EXCHG.10)
ms:contentKeyID: 55107829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ebb96af18e655c9f9304e2fe7a339663c0206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788988"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="4c486-103">Método Windows8Api. JetOpenTemporaryTable2</span><span class="sxs-lookup"><span data-stu-id="4c486-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="4c486-104">Cria uma tabela temporária com um único índice.</span><span class="sxs-lookup"><span data-stu-id="4c486-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="4c486-105">Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="4c486-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="4c486-106">No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil.</span><span class="sxs-lookup"><span data-stu-id="4c486-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="4c486-107">Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial.</span><span class="sxs-lookup"><span data-stu-id="4c486-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="4c486-108">Consulte também [JetOpenTempTable (JET_SESID, \[ \] Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "API. JetOpenTempTable2", [JetOpenTempTable3 (JET_SESID, \[ \] Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="4c486-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="4c486-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="4c486-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="4c486-110">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4c486-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="4c486-111">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4c486-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4c486-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c486-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable2 ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEWindows8Api.JetOpenTemporaryTable2(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable2(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="4c486-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c486-113">Parameters</span></span>

  - <span data-ttu-id="4c486-114">sesid</span><span class="sxs-lookup"><span data-stu-id="4c486-114">sesid</span></span>  
    <span data-ttu-id="4c486-115">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4c486-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4c486-116">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4c486-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4c486-117">temporáriotable</span><span class="sxs-lookup"><span data-stu-id="4c486-117">temporarytable</span></span>  
    <span data-ttu-id="4c486-118">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="4c486-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="4c486-119">Descrição da tabela temporária a ser criada na entrada.</span><span class="sxs-lookup"><span data-stu-id="4c486-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="4c486-120">Após uma chamada bem-sucedida, a estrutura contém o identificador para a tabela temporária e as identificações de coluna.</span><span class="sxs-lookup"><span data-stu-id="4c486-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="4c486-121">Use [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) para liberar a tabela temporária quando terminar.</span><span class="sxs-lookup"><span data-stu-id="4c486-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c486-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c486-122">Remarks</span></span>

<span data-ttu-id="4c486-123">Use [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) para versões anteriores do ESENT.</span><span class="sxs-lookup"><span data-stu-id="4c486-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c486-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c486-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4c486-125">Referência</span><span class="sxs-lookup"><span data-stu-id="4c486-125">Reference</span></span>

[<span data-ttu-id="4c486-126">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="4c486-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="4c486-127">Membros do Windows8Api</span><span class="sxs-lookup"><span data-stu-id="4c486-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="4c486-128">Namespace Microsoft. ISAM. ESENT. Interop. windows8</span><span class="sxs-lookup"><span data-stu-id="4c486-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
