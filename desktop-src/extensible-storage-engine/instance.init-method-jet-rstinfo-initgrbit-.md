---
description: 'Saiba mais sobre: Instance.Inimétodo t (JET_RSTINFO, InitGrbit)'
title: Método t Instance.Ini(JET_RSTINFO, InitGrbit)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784648"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a><span data-ttu-id="196c8-103">Método t Instance.Ini(JET_RSTINFO, InitGrbit)</span><span class="sxs-lookup"><span data-stu-id="196c8-103">Instance.Init method (JET_RSTINFO, InitGrbit)</span></span>

<span data-ttu-id="196c8-104">Inicialize o JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="196c8-104">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="196c8-105">Essa API requer pelo menos a versão vista do ESENT.</span><span class="sxs-lookup"><span data-stu-id="196c8-105">This API requires at least the Vista version of ESENT.</span></span>

<span data-ttu-id="196c8-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="196c8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="196c8-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="196c8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="196c8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="196c8-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="196c8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="196c8-109">Parameters</span></span>

  - <span data-ttu-id="196c8-110">recuperação de</span><span class="sxs-lookup"><span data-stu-id="196c8-110">recoveryOptions</span></span>  
    <span data-ttu-id="196c8-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="196c8-111">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="196c8-112">Parâmetros de recuperação adicionais para remapear bancos de dados durante a recuperação, posicione onde parar a recuperação ou status de recuperação.</span><span class="sxs-lookup"><span data-stu-id="196c8-112">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="196c8-113">grbit</span><span class="sxs-lookup"><span data-stu-id="196c8-113">grbit</span></span>  
    <span data-ttu-id="196c8-114">Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="196c8-114">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="196c8-115">Opções de inicialização.</span><span class="sxs-lookup"><span data-stu-id="196c8-115">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="196c8-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="196c8-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="196c8-117">Referência</span><span class="sxs-lookup"><span data-stu-id="196c8-117">Reference</span></span>

[<span data-ttu-id="196c8-118">Classe de instância</span><span class="sxs-lookup"><span data-stu-id="196c8-118">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="196c8-119">Membros da Instância </span><span class="sxs-lookup"><span data-stu-id="196c8-119">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="196c8-120">Sobrecarga de init</span><span class="sxs-lookup"><span data-stu-id="196c8-120">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="196c8-121">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="196c8-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
