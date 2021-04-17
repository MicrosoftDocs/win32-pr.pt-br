---
description: 'Saiba mais sobre a propriedade: Instanceparameters. PageTempDBMin'
title: Propriedade instanceparameters. PageTempDBMin
TOCTitle: 'PageTempDBMin property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.pagetempdbmin(v=EXCHG.10)
ms:contentKeyID: 55103558
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06825762485ad52743d585ce0fed86bd1739cd21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762123"
---
# <a name="instanceparameterspagetempdbmin-property"></a><span data-ttu-id="2161c-103">Propriedade instanceparameters. PageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="2161c-103">InstanceParameters.PageTempDBMin property</span></span>

<span data-ttu-id="2161c-104">Obtém ou define o tamanho inicial do banco de dados temporário.</span><span class="sxs-lookup"><span data-stu-id="2161c-104">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="2161c-105">O tamanho está em páginas de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2161c-105">The size is in database pages.</span></span> <span data-ttu-id="2161c-106">Um tamanho de zero indica que o tamanho padrão de um banco de dados comum deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="2161c-106">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="2161c-107">Geralmente, é desejável que aplicativos pequenos configurem o banco de dados temporário para que seja o menor possível.</span><span class="sxs-lookup"><span data-stu-id="2161c-107">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="2161c-108">Definir esse parâmetro como [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) atingirá o menor banco de dados temporário possível.</span><span class="sxs-lookup"><span data-stu-id="2161c-108">Setting this parameter to [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) will achieve the smallest temporary database possible.</span></span>

<span data-ttu-id="2161c-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2161c-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2161c-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2161c-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2161c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2161c-111">Syntax</span></span>

``` vb
'Declaration
Public Property PageTempDBMin As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PageTempDBMin

instance.PageTempDBMin = value
```

``` csharp
public int PageTempDBMin { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="2161c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2161c-112">Property value</span></span>

<span data-ttu-id="2161c-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2161c-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2161c-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="2161c-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2161c-115">Referência</span><span class="sxs-lookup"><span data-stu-id="2161c-115">Reference</span></span>

[<span data-ttu-id="2161c-116">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="2161c-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="2161c-117">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="2161c-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="2161c-118">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2161c-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
