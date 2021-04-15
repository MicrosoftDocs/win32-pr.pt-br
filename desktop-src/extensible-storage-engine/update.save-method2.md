---
description: 'Saiba mais sobre: método Update. Save'
title: Método Update. Save
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57693d3952f011127e60fdfb70dd2352c2f15207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501903"
---
# <a name="updatesave-method"></a><span data-ttu-id="d56ea-103">Método Update. Save</span><span class="sxs-lookup"><span data-stu-id="d56ea-103">Update.Save method</span></span>

<span data-ttu-id="d56ea-104">Atualize o TableName.</span><span class="sxs-lookup"><span data-stu-id="d56ea-104">Update the tableid.</span></span>

<span data-ttu-id="d56ea-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d56ea-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d56ea-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d56ea-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d56ea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d56ea-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a><span data-ttu-id="d56ea-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="d56ea-108">Remarks</span></span>

<span data-ttu-id="d56ea-109">Save é a etapa final na execução de uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="d56ea-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="d56ea-110">A atualização é iniciada chamando a criação de um objeto de atualização e, em seguida, chamando JetSetColumn ou JetSetColumns uma ou mais vezes para definir o estado do registro.</span><span class="sxs-lookup"><span data-stu-id="d56ea-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="d56ea-111">Por fim, a atualização é chamada para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="d56ea-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="d56ea-112">Os índices são atualizados somente pela atualização ou e não durante JetSetColumn ou JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="d56ea-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="d56ea-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="d56ea-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d56ea-114">Referência</span><span class="sxs-lookup"><span data-stu-id="d56ea-114">Reference</span></span>

[<span data-ttu-id="d56ea-115">Atualizar classe</span><span class="sxs-lookup"><span data-stu-id="d56ea-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="d56ea-116">Atualizar Membros</span><span class="sxs-lookup"><span data-stu-id="d56ea-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="d56ea-117">Salvar sobrecarga</span><span class="sxs-lookup"><span data-stu-id="d56ea-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="d56ea-118">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d56ea-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
