---
description: 'Saiba mais sobre: método Update. SaveAndGotoBookmark'
title: Método Update. SaveAndGotoBookmark
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808215"
---
# <a name="updatesaveandgotobookmark-method"></a><span data-ttu-id="22119-103">Método Update. SaveAndGotoBookmark</span><span class="sxs-lookup"><span data-stu-id="22119-103">Update.SaveAndGotoBookmark method</span></span>

<span data-ttu-id="22119-104">Atualize a TableName e posicione a TableName no registro que foi modificado.</span><span class="sxs-lookup"><span data-stu-id="22119-104">Update the tableid and position the tableid on the record that was modified.</span></span> <span data-ttu-id="22119-105">Isso pode ser útil ao inserir um registro porque, por padrão, o TableName permanece em seu local antigo.</span><span class="sxs-lookup"><span data-stu-id="22119-105">This can be useful when inserting a record because by default the tableid remains in its old location.</span></span>

<span data-ttu-id="22119-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22119-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22119-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="22119-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22119-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22119-108">Syntax</span></span>

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a><span data-ttu-id="22119-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="22119-109">Remarks</span></span>

<span data-ttu-id="22119-110">Save é a etapa final na execução de uma inserção ou atualização.</span><span class="sxs-lookup"><span data-stu-id="22119-110">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="22119-111">A atualização é iniciada chamando a criação de um objeto de atualização e, em seguida, chamando JetSetColumn ou JetSetColumns uma ou mais vezes para definir o estado do registro.</span><span class="sxs-lookup"><span data-stu-id="22119-111">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="22119-112">Por fim, a atualização é chamada para concluir a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="22119-112">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="22119-113">Os índices são atualizados somente pela atualização ou e não durante JetSetColumn ou JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="22119-113">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="22119-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="22119-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22119-115">Referência</span><span class="sxs-lookup"><span data-stu-id="22119-115">Reference</span></span>

[<span data-ttu-id="22119-116">Atualizar classe</span><span class="sxs-lookup"><span data-stu-id="22119-116">Update class</span></span>](./update-class.md)

[<span data-ttu-id="22119-117">Atualizar Membros</span><span class="sxs-lookup"><span data-stu-id="22119-117">Update members</span></span>](./update-members.md)

[<span data-ttu-id="22119-118">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="22119-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
