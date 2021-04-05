---
description: 'Saiba mais sobre a propriedade: Instanceparameters. CachedClosedTables'
title: Propriedade instanceparameters. CachedClosedTables
TOCTitle: 'CachedClosedTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55103293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachedClosedTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f2465de2df3d25293f5298d40700512b6a086d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661500"
---
# <a name="instanceparameterscachedclosedtables-property"></a><span data-ttu-id="4120e-103">Propriedade instanceparameters. CachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="4120e-103">InstanceParameters.CachedClosedTables property</span></span>

<span data-ttu-id="4120e-104">Obtém ou define um valor que concede o número de recursos de árvore B em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4120e-104">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="4120e-105">Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4120e-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="4120e-106">Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.</span><span class="sxs-lookup"><span data-stu-id="4120e-106">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="4120e-107">Com suporte no Windows Vista e em cima.</span><span class="sxs-lookup"><span data-stu-id="4120e-107">Supported on Windows Vista and up.</span></span> <span data-ttu-id="4120e-108">Ignorado no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4120e-108">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="4120e-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4120e-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4120e-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4120e-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4120e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4120e-111">Syntax</span></span>

``` vb
'Declaration
Public Property CachedClosedTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachedClosedTables

instance.CachedClosedTables = value
```

``` csharp
public int CachedClosedTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="4120e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4120e-112">Property value</span></span>

<span data-ttu-id="4120e-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4120e-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4120e-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="4120e-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4120e-115">Referência</span><span class="sxs-lookup"><span data-stu-id="4120e-115">Reference</span></span>

[<span data-ttu-id="4120e-116">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="4120e-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="4120e-117">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="4120e-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="4120e-118">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4120e-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
