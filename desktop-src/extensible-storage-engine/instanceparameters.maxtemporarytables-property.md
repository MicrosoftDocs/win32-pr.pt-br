---
description: 'Saiba mais sobre a propriedade: Instanceparameters. MaxTemporaryTables'
title: Propriedade instanceparameters. MaxTemporaryTables
TOCTitle: 'MaxTemporaryTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtemporarytables(v=EXCHG.10)
ms:contentKeyID: 55103560
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTemporaryTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5802e512a4ea6a4916ae54c24357dbdad057540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105802063"
---
# <a name="instanceparametersmaxtemporarytables-property"></a><span data-ttu-id="6d3ec-103">Propriedade instanceparameters. MaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="6d3ec-103">InstanceParameters.MaxTemporaryTables property</span></span>

<span data-ttu-id="6d3ec-104">Obtém ou define o número de recursos de tabela temporária para uso por uma instância.</span><span class="sxs-lookup"><span data-stu-id="6d3ec-104">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="6d3ec-105">Essa configuração afetará quantas tabelas temporárias podem ser usadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6d3ec-105">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="6d3ec-106">Se esse parâmetro de sistema for definido como zero, nenhum banco de dados temporário será criado e qualquer atividade que exija o uso do banco de dados temporário falhará.</span><span class="sxs-lookup"><span data-stu-id="6d3ec-106">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="6d3ec-107">Essa configuração pode ser útil para evitar a e/s necessária para criar o banco de dados temporário se for conhecido que ele não será usado.</span><span class="sxs-lookup"><span data-stu-id="6d3ec-107">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="6d3ec-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6d3ec-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6d3ec-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6d3ec-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3ec-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d3ec-110">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTemporaryTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTemporaryTables

instance.MaxTemporaryTables = value
```

``` csharp
public int MaxTemporaryTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="6d3ec-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6d3ec-111">Property value</span></span>

<span data-ttu-id="6d3ec-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6d3ec-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="remarks"></a><span data-ttu-id="6d3ec-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d3ec-113">Remarks</span></span>

<span data-ttu-id="6d3ec-114">O uso de uma tabela temporária também requer um recurso de cursor.</span><span class="sxs-lookup"><span data-stu-id="6d3ec-114">The use of a temporary table also requires a cursor resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d3ec-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d3ec-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6d3ec-116">Referência</span><span class="sxs-lookup"><span data-stu-id="6d3ec-116">Reference</span></span>

[<span data-ttu-id="6d3ec-117">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="6d3ec-117">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="6d3ec-118">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="6d3ec-118">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="6d3ec-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6d3ec-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
