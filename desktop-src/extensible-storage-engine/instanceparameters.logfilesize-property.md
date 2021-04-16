---
description: 'Saiba mais sobre a propriedade: Instanceparameters. LogFileSize'
title: Propriedade instanceparameters. LogFileSize
TOCTitle: 'LogFileSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfilesize(v=EXCHG.10)
ms:contentKeyID: 55103312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c141c76a92f49b4b5000cad65e302a7cf15d780f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765305"
---
# <a name="instanceparameterslogfilesize-property"></a><span data-ttu-id="818ae-103">Propriedade instanceparameters. LogFileSize</span><span class="sxs-lookup"><span data-stu-id="818ae-103">InstanceParameters.LogFileSize property</span></span>

<span data-ttu-id="818ae-104">Obtém ou define o tamanho dos arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="818ae-104">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="818ae-105">Esse parâmetro deve ser definido em unidades de 1024 bytes (por exemplo, uma configuração de 2048 fornecerá arquivos de log de 2 MB).</span><span class="sxs-lookup"><span data-stu-id="818ae-105">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span>

<span data-ttu-id="818ae-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="818ae-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="818ae-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="818ae-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="818ae-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="818ae-108">Syntax</span></span>

``` vb
'Declaration
Public Property LogFileSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogFileSize

instance.LogFileSize = value
```

``` csharp
public int LogFileSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="818ae-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="818ae-109">Property value</span></span>

<span data-ttu-id="818ae-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="818ae-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="818ae-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="818ae-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="818ae-112">Referência</span><span class="sxs-lookup"><span data-stu-id="818ae-112">Reference</span></span>

[<span data-ttu-id="818ae-113">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="818ae-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="818ae-114">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="818ae-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="818ae-115">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="818ae-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
