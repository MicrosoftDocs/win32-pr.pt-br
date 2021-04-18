---
description: 'Saiba mais sobre a propriedade: Instanceparameters. LogBuffers'
title: Propriedade instanceparameters. LogBuffers
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768205"
---
# <a name="instanceparameterslogbuffers-property"></a><span data-ttu-id="28bf1-103">Propriedade instanceparameters. LogBuffers</span><span class="sxs-lookup"><span data-stu-id="28bf1-103">InstanceParameters.LogBuffers property</span></span>

<span data-ttu-id="28bf1-104">Obtém ou define a quantidade de memória usada para armazenar em cache os registros de log antes que eles sejam gravados no arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="28bf1-104">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="28bf1-105">A unidade para esse parâmetro é o tamanho do setor do volume que contém os arquivos de log de transações.</span><span class="sxs-lookup"><span data-stu-id="28bf1-105">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="28bf1-106">O tamanho do setor quase sempre é de 512 bytes, portanto, é seguro assumir esse tamanho para a unidade.</span><span class="sxs-lookup"><span data-stu-id="28bf1-106">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="28bf1-107">Esse parâmetro tem um impacto no desempenho.</span><span class="sxs-lookup"><span data-stu-id="28bf1-107">This parameter has an impact on performance.</span></span> <span data-ttu-id="28bf1-108">Quando o mecanismo de banco de dados está sob carga de atualização pesada, esse buffer pode se tornar completo com muita rapidez.</span><span class="sxs-lookup"><span data-stu-id="28bf1-108">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="28bf1-109">Um tamanho de cache maior para o arquivo de log de transações é essencial para um bom desempenho de atualização sob uma condição de alta carga.</span><span class="sxs-lookup"><span data-stu-id="28bf1-109">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="28bf1-110">O padrão é conhecido como muito pequeno para esse caso.</span><span class="sxs-lookup"><span data-stu-id="28bf1-110">The default is known to be too small for this case.</span></span> <span data-ttu-id="28bf1-111">Não defina esse parâmetro como um número de buffers que seja maior (em bytes) que metade do tamanho de um arquivo de log de transações.</span><span class="sxs-lookup"><span data-stu-id="28bf1-111">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<span data-ttu-id="28bf1-112">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="28bf1-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="28bf1-113">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="28bf1-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="28bf1-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28bf1-114">Syntax</span></span>

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="28bf1-115">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="28bf1-115">Property value</span></span>

<span data-ttu-id="28bf1-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="28bf1-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="28bf1-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="28bf1-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="28bf1-118">Referência</span><span class="sxs-lookup"><span data-stu-id="28bf1-118">Reference</span></span>

[<span data-ttu-id="28bf1-119">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="28bf1-119">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="28bf1-120">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="28bf1-120">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="28bf1-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="28bf1-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
