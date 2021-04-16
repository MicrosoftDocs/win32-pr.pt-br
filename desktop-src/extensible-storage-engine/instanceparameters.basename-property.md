---
description: 'Saiba mais sobre a propriedade: Instanceparameters. BaseName'
title: Propriedade instanceparameters. BaseName
TOCTitle: 'BaseName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.basename(v=EXCHG.10)
ms:contentKeyID: 55103315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_BaseName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d7e36363a73dc19c324e1852f58346e0ad95b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772962"
---
# <a name="instanceparametersbasename-property"></a><span data-ttu-id="7917d-103">Propriedade instanceparameters. BaseName</span><span class="sxs-lookup"><span data-stu-id="7917d-103">InstanceParameters.BaseName property</span></span>

<span data-ttu-id="7917d-104">Obtém ou define o prefixo de três letras usado para muitos dos arquivos usados pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7917d-104">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="7917d-105">Por exemplo, o arquivo de ponto de verificação é chamado de EDB. CHK por padrão, porque o EDB é o nome de base padrão.</span><span class="sxs-lookup"><span data-stu-id="7917d-105">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span>

<span data-ttu-id="7917d-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7917d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7917d-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7917d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7917d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7917d-108">Syntax</span></span>

``` vb
'Declaration
Public Property BaseName As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.BaseName

instance.BaseName = value
```

``` csharp
public string BaseName { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="7917d-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7917d-109">Property value</span></span>

<span data-ttu-id="7917d-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7917d-110">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7917d-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="7917d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7917d-112">Referência</span><span class="sxs-lookup"><span data-stu-id="7917d-112">Reference</span></span>

[<span data-ttu-id="7917d-113">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="7917d-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="7917d-114">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="7917d-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="7917d-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7917d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
