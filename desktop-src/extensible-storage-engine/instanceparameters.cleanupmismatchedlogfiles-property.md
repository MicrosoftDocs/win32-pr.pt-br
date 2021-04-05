---
description: 'Saiba mais sobre a propriedade: Instanceparameters. CleanupMismatchedLogFiles'
title: Propriedade instanceparameters. CleanupMismatchedLogFiles
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091075"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a><span data-ttu-id="90961-103">Propriedade instanceparameters. CleanupMismatchedLogFiles</span><span class="sxs-lookup"><span data-stu-id="90961-103">InstanceParameters.CleanupMismatchedLogFiles property</span></span>

<span data-ttu-id="90961-104">Obtém ou define um valor que indica se JetInit falha quando o mecanismo de banco de dados é configurado para começar a usar arquivos de log de transações em um disco que tenha um tamanho diferente do que está configurado.</span><span class="sxs-lookup"><span data-stu-id="90961-104">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="90961-105">Normalmente, [JetInit (JET_INSTANCE)](./api.jetinit-method.md) recuperará com êxito os bancos de dados, mas falhará com [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) para indicar que o tamanho do arquivo de log está configurado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="90961-105">Normally, [JetInit(JET_INSTANCE)](./api.jetinit-method.md) will successfully recover the databases but will fail with [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="90961-106">No entanto, quando esse parâmetro for definido como true, o mecanismo de banco de dados excluirá silenciosamente todos os arquivos de log antigos, iniciará um novo conjunto de arquivos de log de transações usando o tamanho do arquivo de log configurado.</span><span class="sxs-lookup"><span data-stu-id="90961-106">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="90961-107">Esse parâmetro é útil quando o aplicativo deseja alterar de forma transparente o tamanho do arquivo de log de transações e ainda funcionar de forma transparente nos cenários de atualização e restauração.</span><span class="sxs-lookup"><span data-stu-id="90961-107">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<span data-ttu-id="90961-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="90961-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="90961-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="90961-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="90961-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="90961-110">Syntax</span></span>

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="90961-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="90961-111">Property value</span></span>

<span data-ttu-id="90961-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="90961-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="90961-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="90961-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90961-114">Referência</span><span class="sxs-lookup"><span data-stu-id="90961-114">Reference</span></span>

[<span data-ttu-id="90961-115">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="90961-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="90961-116">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="90961-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="90961-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="90961-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
