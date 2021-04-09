---
description: 'Saiba mais sobre: método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, PrereadKeysGrbit)'
title: Método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, PrereadKeysGrbit) (Microsoft. ISAM. ESENT. Interop. windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55107785
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66f85c08c1fccc58702d4ac4cf170d6b0493ab8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010353"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-prereadkeysgrbit"></a><span data-ttu-id="e9fe0-103">Método Windows7Api. JetPrereadKeys (JET_SESID, JET_TABLEID, byte \[ \] \[ \] , Int32, Int32, Int32, PrereadKeysGrbit)</span><span class="sxs-lookup"><span data-stu-id="e9fe0-103">Windows7Api.JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte\[\]\[\], Int32 , Int32, Int32, PrereadKeysGrbit)</span></span>

<span data-ttu-id="e9fe0-104">Se os registros com as chaves especificadas não estiverem no cache do buffer, inicie as leituras assíncronas para colocar os registros no cache do buffer de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-104">If the records with the specified keys are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="e9fe0-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e9fe0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="e9fe0-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e9fe0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e9fe0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9fe0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyCount, keysPreread, _
    grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e9fe0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9fe0-108">Parameters</span></span>

  - <span data-ttu-id="e9fe0-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e9fe0-109">sesid</span></span>  
    <span data-ttu-id="e9fe0-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9fe0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e9fe0-111">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9fe0-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e9fe0-112">tableid</span></span>  
    <span data-ttu-id="e9fe0-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e9fe0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e9fe0-114">A tabela na qual os itens são relidos.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9fe0-115">chaves</span><span class="sxs-lookup"><span data-stu-id="e9fe0-115">keys</span></span>  
    <span data-ttu-id="e9fe0-116">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="e9fe0-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="e9fe0-117">As chaves a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-117">The keys to preread.</span></span> <span data-ttu-id="e9fe0-118">As chaves devem ser classificadas.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-118">The keys must be sorted.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9fe0-119">Comprimentos de caracteres</span><span class="sxs-lookup"><span data-stu-id="e9fe0-119">keyLengths</span></span>  
    <span data-ttu-id="e9fe0-120">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="e9fe0-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="e9fe0-121">Os comprimentos das chaves a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-121">The lengths of the keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9fe0-122">Contagem de keycount</span><span class="sxs-lookup"><span data-stu-id="e9fe0-122">keyCount</span></span>  
    <span data-ttu-id="e9fe0-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e9fe0-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e9fe0-124">O número máximo de chaves a serem lidas.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-124">The maximum number of keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9fe0-125">keysPreread</span><span class="sxs-lookup"><span data-stu-id="e9fe0-125">keysPreread</span></span>  
    <span data-ttu-id="e9fe0-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e9fe0-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e9fe0-127">Retorna o número de chaves para realmente ser lido.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-127">Returns the number of keys to actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e9fe0-128">grbit</span><span class="sxs-lookup"><span data-stu-id="e9fe0-128">grbit</span></span>  
    <span data-ttu-id="e9fe0-129">Tipo: [Microsoft. ISAM. ESENT. Interop. Windows7. PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e9fe0-129">Type: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e9fe0-130">Opções de preread.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-130">Preread options.</span></span> <span data-ttu-id="e9fe0-131">Usado para especificar a direção da subleitura.</span><span class="sxs-lookup"><span data-stu-id="e9fe0-131">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9fe0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9fe0-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e9fe0-133">Referência</span><span class="sxs-lookup"><span data-stu-id="e9fe0-133">Reference</span></span>

[<span data-ttu-id="e9fe0-134">Classe Windows7Api</span><span class="sxs-lookup"><span data-stu-id="e9fe0-134">Windows7Api class</span></span>](./windows7api-class.md)

[<span data-ttu-id="e9fe0-135">Membros do Windows7Api</span><span class="sxs-lookup"><span data-stu-id="e9fe0-135">Windows7Api members</span></span>](./windows7api-members.md)

[<span data-ttu-id="e9fe0-136">Sobrecarga de JetPrereadKeys</span><span class="sxs-lookup"><span data-stu-id="e9fe0-136">JetPrereadKeys overload</span></span>](./windows7api.jetprereadkeys-method.md)

[<span data-ttu-id="e9fe0-137">Namespace Microsoft. ISAM. ESENT. Interop. Windows7</span><span class="sxs-lookup"><span data-stu-id="e9fe0-137">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
