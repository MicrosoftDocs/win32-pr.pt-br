---
description: 'Saiba mais sobre: SystemParameters.ConfigPropriedade uração'
title: SystemParameters.ConfigPropriedade uração
TOCTitle: 'Configuration property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.configuration(v=EXCHG.10)
ms:contentKeyID: 55104117
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.set_Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.get_Configuration
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eaa387f63df1dd91641ff38f2a6f6450629fe99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828631"
---
# <a name="systemparametersconfiguration-property"></a><span data-ttu-id="aadd9-103">SystemParameters.ConfigPropriedade uração</span><span class="sxs-lookup"><span data-stu-id="aadd9-103">SystemParameters.Configuration property</span></span>

<span data-ttu-id="aadd9-104">Obtém ou define um valor que especifica os valores padrão para o conjunto inteiro de parâmetros do sistema.</span><span class="sxs-lookup"><span data-stu-id="aadd9-104">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="aadd9-105">Quando esse parâmetro é definido como uma configuração específica, todos os valores de parâmetro do sistema são redefinidos para seus valores padrão para essa configuração.</span><span class="sxs-lookup"><span data-stu-id="aadd9-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="aadd9-106">Se a configuração for definida para uma instância específica, os parâmetros do sistema global não serão redefinidos para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="aadd9-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="aadd9-107">Configuração pequena (0): o mecanismo de banco de dados é otimizado para uso de memória.</span><span class="sxs-lookup"><span data-stu-id="aadd9-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="aadd9-108">Configuração herdada (1): o mecanismo de banco de dados tem seus padrões tradicionais.</span><span class="sxs-lookup"><span data-stu-id="aadd9-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="aadd9-109">Com suporte no Windows Vista e em cima.</span><span class="sxs-lookup"><span data-stu-id="aadd9-109">Supported on Windows Vista and up.</span></span> <span data-ttu-id="aadd9-110">Ignorado no Windows XP e no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="aadd9-110">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="aadd9-111">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aadd9-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aadd9-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aadd9-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aadd9-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="aadd9-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property Configuration As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.Configuration

SystemParameters.Configuration = value
```

``` csharp
public static int Configuration { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="aadd9-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="aadd9-114">Property value</span></span>

<span data-ttu-id="aadd9-115">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="aadd9-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="aadd9-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="aadd9-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aadd9-117">Referência</span><span class="sxs-lookup"><span data-stu-id="aadd9-117">Reference</span></span>

[<span data-ttu-id="aadd9-118">Classe SystemParameters</span><span class="sxs-lookup"><span data-stu-id="aadd9-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="aadd9-119">Membros do SystemParameters</span><span class="sxs-lookup"><span data-stu-id="aadd9-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="aadd9-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="aadd9-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
