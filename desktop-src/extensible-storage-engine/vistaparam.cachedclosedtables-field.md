---
description: 'Saiba mais sobre: campo VistaParam. CachedClosedTables'
title: Campo VistaParam. CachedClosedTables (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff72925e34c731e57d11170753ecff13f4b96a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089871"
---
# <a name="vistaparamcachedclosedtables-field"></a><span data-ttu-id="0678b-103">Campo VistaParam. CachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="0678b-103">VistaParam.CachedClosedTables field</span></span>

<span data-ttu-id="0678b-104">Esse parâmetro controla o número de recursos da árvore B + em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0678b-104">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="0678b-105">Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0678b-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="0678b-106">Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.</span><span class="sxs-lookup"><span data-stu-id="0678b-106">This is useful for applications that have a schema with a very large number of tables.</span></span>

<span data-ttu-id="0678b-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0678b-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="0678b-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0678b-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0678b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0678b-109">Syntax</span></span>

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a><span data-ttu-id="0678b-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="0678b-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0678b-111">Referência</span><span class="sxs-lookup"><span data-stu-id="0678b-111">Reference</span></span>

[<span data-ttu-id="0678b-112">Classe VistaParam</span><span class="sxs-lookup"><span data-stu-id="0678b-112">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="0678b-113">Membros do VistaParam</span><span class="sxs-lookup"><span data-stu-id="0678b-113">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="0678b-114">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="0678b-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
