---
description: 'Saiba mais sobre: método VistaApi. JetOpenTemporaryTable'
title: Método VistaApi. JetOpenTemporaryTable (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798550"
---
# <a name="vistaapijetopentemporarytable-method"></a><span data-ttu-id="ec457-103">Método VistaApi. JetOpenTemporaryTable</span><span class="sxs-lookup"><span data-stu-id="ec457-103">VistaApi.JetOpenTemporaryTable method</span></span>

<span data-ttu-id="ec457-104">Cria uma tabela temporária com um único índice.</span><span class="sxs-lookup"><span data-stu-id="ec457-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="ec457-105">Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="ec457-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="ec457-106">No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil.</span><span class="sxs-lookup"><span data-stu-id="ec457-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="ec457-107">Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial.</span><span class="sxs-lookup"><span data-stu-id="ec457-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="ec457-108">Consulte também [JetOpenTempTable (JET_SESID, \[ \] Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="ec457-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span>

<span data-ttu-id="ec457-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec457-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ec457-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ec457-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec457-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec457-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="ec457-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec457-112">Parameters</span></span>

  - <span data-ttu-id="ec457-113">sesid</span><span class="sxs-lookup"><span data-stu-id="ec457-113">sesid</span></span>  
    <span data-ttu-id="ec457-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ec457-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ec457-115">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="ec457-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ec457-116">temporáriotable</span><span class="sxs-lookup"><span data-stu-id="ec457-116">temporarytable</span></span>  
    <span data-ttu-id="ec457-117">Tipo: [Microsoft.ISAM.ESENT.Interop.vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="ec457-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="ec457-118">Descrição da tabela temporária a ser criada na entrada.</span><span class="sxs-lookup"><span data-stu-id="ec457-118">Description of the temporary table to create on input.</span></span> <span data-ttu-id="ec457-119">Após uma chamada bem-sucedida, a estrutura contém o identificador para a tabela temporária e as identificações de coluna.</span><span class="sxs-lookup"><span data-stu-id="ec457-119">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="ec457-120">Use [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) para liberar a tabela temporária quando terminar.</span><span class="sxs-lookup"><span data-stu-id="ec457-120">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec457-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec457-121">Remarks</span></span>

<span data-ttu-id="ec457-122">Introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ec457-122">Introduced in Windows Vista.</span></span> <span data-ttu-id="ec457-123">Use [JetOpenTempTable3 (JET_SESID, \[ \] Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md) para versões anteriores do ESENT.</span><span class="sxs-lookup"><span data-stu-id="ec457-123">Use [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec457-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec457-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec457-125">Referência</span><span class="sxs-lookup"><span data-stu-id="ec457-125">Reference</span></span>

[<span data-ttu-id="ec457-126">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="ec457-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="ec457-127">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="ec457-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="ec457-128">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="ec457-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
