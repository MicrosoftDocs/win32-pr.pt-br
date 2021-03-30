---
description: 'Saiba mais sobre: VistaParam.Configcampo uração'
title: VistaParam.Configcampo uração (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646698"
---
# <a name="vistaparamconfiguration-field"></a><span data-ttu-id="dfdb4-103">VistaParam.Configcampo uração</span><span class="sxs-lookup"><span data-stu-id="dfdb4-103">VistaParam.Configuration field</span></span>

<span data-ttu-id="dfdb4-104">Esse parâmetro expõe vários conjuntos de valores padrão para todo o conjunto de parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="dfdb4-104">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="dfdb4-105">Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="dfdb4-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="dfdb4-106">Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="dfdb4-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="dfdb4-107">Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória.</span><span class="sxs-lookup"><span data-stu-id="dfdb4-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="dfdb4-108">Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais.</span><span class="sxs-lookup"><span data-stu-id="dfdb4-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="dfdb4-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dfdb4-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="dfdb4-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dfdb4-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dfdb4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfdb4-111">Syntax</span></span>

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a><span data-ttu-id="dfdb4-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfdb4-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dfdb4-113">Referência</span><span class="sxs-lookup"><span data-stu-id="dfdb4-113">Reference</span></span>

[<span data-ttu-id="dfdb4-114">Classe VistaParam</span><span class="sxs-lookup"><span data-stu-id="dfdb4-114">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="dfdb4-115">Membros do VistaParam</span><span class="sxs-lookup"><span data-stu-id="dfdb4-115">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="dfdb4-116">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="dfdb4-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
