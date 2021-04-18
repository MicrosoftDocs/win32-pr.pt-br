---
description: 'Saiba mais sobre a propriedade: Instanceparameters. AlternateDatabaseRecoveryDirectory'
title: Propriedade instanceparameters. AlternateDatabaseRecoveryDirectory
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813989"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a><span data-ttu-id="2c1f5-103">Propriedade instanceparameters. AlternateDatabaseRecoveryDirectory</span><span class="sxs-lookup"><span data-stu-id="2c1f5-103">InstanceParameters.AlternateDatabaseRecoveryDirectory property</span></span>

<span data-ttu-id="2c1f5-104">Obtém ou define o caminho relativo ou absoluto do sistema de arquivos de uma pasta na qual a recuperação de falha ou uma operação de restauração pode encontrar os bancos de dados referenciados no log de transações na pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="2c1f5-104">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="2c1f5-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2c1f5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2c1f5-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2c1f5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2c1f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c1f5-107">Syntax</span></span>

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="2c1f5-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2c1f5-108">Property value</span></span>

<span data-ttu-id="2c1f5-109">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2c1f5-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="remarks"></a><span data-ttu-id="2c1f5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c1f5-110">Remarks</span></span>

<span data-ttu-id="2c1f5-111">Esse parâmetro é ignorado no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c1f5-111">This parameter is ignored on Windows XP.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c1f5-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c1f5-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2c1f5-113">Referência</span><span class="sxs-lookup"><span data-stu-id="2c1f5-113">Reference</span></span>

[<span data-ttu-id="2c1f5-114">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="2c1f5-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="2c1f5-115">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="2c1f5-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="2c1f5-116">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2c1f5-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
