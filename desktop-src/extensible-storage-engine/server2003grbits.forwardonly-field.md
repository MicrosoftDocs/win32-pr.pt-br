---
description: 'Saiba mais sobre: campo Server2003Grbits. ForwardOnly'
title: Campo Server2003Grbits. ForwardOnly (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec4427628e8d6bfee427fa91c15ed6aee3887314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090875"
---
# <a name="server2003grbitsforwardonly-field"></a><span data-ttu-id="8c42c-103">Campo Server2003Grbits. ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="8c42c-103">Server2003Grbits.ForwardOnly field</span></span>

<span data-ttu-id="8c42c-104">Essa opção solicita que a tabela temporária só seja criada se o Gerenciador de tabelas temporárias puder usar a implementação otimizada para resultados de consulta intermediários.</span><span class="sxs-lookup"><span data-stu-id="8c42c-104">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="8c42c-105">Se qualquer característica da tabela temporária impedir o uso dessa otimização, a operação falhará com JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="8c42c-105">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="8c42c-106">Um efeito colateral dessa opção é permitir que a tabela temporária contenha registros com chaves de índice duplicadas.</span><span class="sxs-lookup"><span data-stu-id="8c42c-106">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="8c42c-107">Consulte [exclusivo](./temptablegrbit-enumeration.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="8c42c-107">See [Unique](./temptablegrbit-enumeration.md) for more information.</span></span>

<span data-ttu-id="8c42c-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c42c-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="8c42c-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c42c-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c42c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c42c-110">Syntax</span></span>

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a><span data-ttu-id="8c42c-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c42c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c42c-112">Referência</span><span class="sxs-lookup"><span data-stu-id="8c42c-112">Reference</span></span>

[<span data-ttu-id="8c42c-113">Classe Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="8c42c-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="8c42c-114">Membros do Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="8c42c-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="8c42c-115">Namespace Microsoft. ISAM. ESENT. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="8c42c-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
