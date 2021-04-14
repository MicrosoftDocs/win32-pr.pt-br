---
description: 'Saiba mais sobre: método Update. Save (Byte, Int32, Int32)'
title: Método Update. Save (Byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461168"
---
# <a name="updatesave-method-byte--int32-int32"></a><span data-ttu-id="5bf96-103">Método Update. Save (Byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="5bf96-103">Update.Save method (Byte , Int32, Int32)</span></span>

<span data-ttu-id="5bf96-104">Atualize o TableName.</span><span class="sxs-lookup"><span data-stu-id="5bf96-104">Update the tableid.</span></span>

<span data-ttu-id="5bf96-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5bf96-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5bf96-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5bf96-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf96-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bf96-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="5bf96-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bf96-108">Parameters</span></span>

  - <span data-ttu-id="5bf96-109">indicador</span><span class="sxs-lookup"><span data-stu-id="5bf96-109">bookmark</span></span>  
    <span data-ttu-id="5bf96-110">Escreva \[\]</span><span class="sxs-lookup"><span data-stu-id="5bf96-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="5bf96-111">Retorna o indicador do registro atualizado.</span><span class="sxs-lookup"><span data-stu-id="5bf96-111">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="5bf96-112">Isso pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="5bf96-112">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bf96-113">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="5bf96-113">bookmarkSize</span></span>  
    <span data-ttu-id="5bf96-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5bf96-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5bf96-115">O tamanho do buffer do indicador.</span><span class="sxs-lookup"><span data-stu-id="5bf96-115">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="5bf96-116">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="5bf96-116">actualBookmarkSize</span></span>  
    <span data-ttu-id="5bf96-117">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5bf96-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5bf96-118">Retorna o tamanho real do indicador.</span><span class="sxs-lookup"><span data-stu-id="5bf96-118">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bf96-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bf96-119">Remarks</span></span>

<span data-ttu-id="5bf96-120">Save é a etapa final na execução de uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="5bf96-120">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="5bf96-121">A atualização é iniciada chamando a criação de um objeto de atualização e, em seguida, chamando JetSetColumn ou JetSetColumns uma ou mais vezes para definir o estado do registro.</span><span class="sxs-lookup"><span data-stu-id="5bf96-121">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="5bf96-122">Por fim, a atualização é chamada para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="5bf96-122">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="5bf96-123">Os índices são atualizados somente pela atualização ou e não durante JetSetColumn ou JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="5bf96-123">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bf96-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bf96-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5bf96-125">Referência</span><span class="sxs-lookup"><span data-stu-id="5bf96-125">Reference</span></span>

[<span data-ttu-id="5bf96-126">Atualizar classe</span><span class="sxs-lookup"><span data-stu-id="5bf96-126">Update class</span></span>](./update-class.md)

[<span data-ttu-id="5bf96-127">Atualizar Membros</span><span class="sxs-lookup"><span data-stu-id="5bf96-127">Update members</span></span>](./update-members.md)

[<span data-ttu-id="5bf96-128">Salvar sobrecarga</span><span class="sxs-lookup"><span data-stu-id="5bf96-128">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="5bf96-129">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5bf96-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
