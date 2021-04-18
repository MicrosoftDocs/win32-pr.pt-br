---
description: 'Saiba mais sobre: método VistaApi. JetInit3'
title: Método VistaApi. JetInit3 (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: 'JetInit3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetinit3(v=EXCHG.10)
ms:contentKeyID: 55104198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c5fa7d1450240a8250e66e2bbe6d8ef0b97c136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760655"
---
# <a name="vistaapijetinit3-method"></a><span data-ttu-id="3bd47-103">Método VistaApi. JetInit3</span><span class="sxs-lookup"><span data-stu-id="3bd47-103">VistaApi.JetInit3 method</span></span>

<span data-ttu-id="3bd47-104">Inicialize o mecanismo de banco de dados ESENT.</span><span class="sxs-lookup"><span data-stu-id="3bd47-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="3bd47-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3bd47-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="3bd47-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3bd47-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd47-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bd47-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetInit3 ( _
    ByRef instance As JET_INSTANCE, _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = VistaApi.JetInit3(instance, _
    recoveryOptions, grbit)
```

``` csharp
public static JET_wrn JetInit3(
    ref JET_INSTANCE instance,
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3bd47-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bd47-108">Parameters</span></span>

  - <span data-ttu-id="3bd47-109">instance</span><span class="sxs-lookup"><span data-stu-id="3bd47-109">instance</span></span>  
    <span data-ttu-id="3bd47-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3bd47-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="3bd47-111">A instância a ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="3bd47-111">The instance to initialize.</span></span> <span data-ttu-id="3bd47-112">Se uma instância não tiver sido alocada, um novo será criado e o mecanismo funcionará no modo de instância única.</span><span class="sxs-lookup"><span data-stu-id="3bd47-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

<!-- end list -->

  - <span data-ttu-id="3bd47-113">recuperação de</span><span class="sxs-lookup"><span data-stu-id="3bd47-113">recoveryOptions</span></span>  
    <span data-ttu-id="3bd47-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="3bd47-114">Type: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)</span></span>  
    
    <span data-ttu-id="3bd47-115">Parâmetros de recuperação adicionais para remapear bancos de dados durante a recuperação, posicione onde parar a recuperação ou status de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3bd47-115">Additional recovery parameters for remapping databases during recovery, position where to stop recovery at, or recovery status.</span></span>

<!-- end list -->

  - <span data-ttu-id="3bd47-116">grbit</span><span class="sxs-lookup"><span data-stu-id="3bd47-116">grbit</span></span>  
    <span data-ttu-id="3bd47-117">Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3bd47-117">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3bd47-118">Opções de inicialização.</span><span class="sxs-lookup"><span data-stu-id="3bd47-118">Initialization options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3bd47-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bd47-119">Return value</span></span>

<span data-ttu-id="3bd47-120">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3bd47-120">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="3bd47-121">Um código de aviso.</span><span class="sxs-lookup"><span data-stu-id="3bd47-121">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3bd47-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bd47-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3bd47-123">Referência</span><span class="sxs-lookup"><span data-stu-id="3bd47-123">Reference</span></span>

[<span data-ttu-id="3bd47-124">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="3bd47-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="3bd47-125">Membros do VistaApi</span><span class="sxs-lookup"><span data-stu-id="3bd47-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="3bd47-126">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="3bd47-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
