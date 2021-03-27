---
description: A classe pai da qual todas as classes de rastreamento de eventos do sistema são derivadas. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: Classe MSNT_SystemTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967467"
---
# <a name="msnt_systemtrace-class"></a><span data-ttu-id="0fb9a-104">\_Classe MSNT SystemTrace</span><span class="sxs-lookup"><span data-stu-id="0fb9a-104">MSNT\_SystemTrace class</span></span>

<span data-ttu-id="0fb9a-105">A classe pai da qual todas as classes de rastreamento de eventos do sistema são derivadas.</span><span class="sxs-lookup"><span data-stu-id="0fb9a-105">The parent class from which all system event trace classes are derived.</span></span>

<span data-ttu-id="0fb9a-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="0fb9a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb9a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fb9a-107">Syntax</span></span>

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a><span data-ttu-id="0fb9a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0fb9a-108">Members</span></span>

<span data-ttu-id="0fb9a-109">A classe **MSNT \_ SystemTrace** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0fb9a-109">The **MSNT\_SystemTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="0fb9a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0fb9a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fb9a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0fb9a-111">Properties</span></span>

<span data-ttu-id="0fb9a-112">A classe **MSNT \_ SystemTrace** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0fb9a-112">The **MSNT\_SystemTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fb9a-113">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="0fb9a-113">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fb9a-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0fb9a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0fb9a-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0fb9a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fb9a-116">Qualificadores: **DefineValues {" \_ \_ \_ processo de sinalizador de rastreamento de eventos", " \_ thread de sinalizador de rastreamento de eventos \_ \_ ", " \_ \_ carregamento de imagem do sinalizador de rastreamento de eventos", "contadores de processo de sinalizador de rastreamento de eventos" \_ \_ \_ \_ \_ \_ , " \_ sinalizador de rastreamento de eventos \_ \_ CSWITCH", " \_ \_ sinal de rastreamento de eventos \_ DPC", " \_ \_ \_ interrupção de sinalizador de rastreamento de eventos", " \_ sinalizador de rastreamento de evento \_ \_ SYSTEMCALL", "sinalizador de rastreamento de eventos \_ \_ \_ \_ e/s de disco", "sinalizador de rastreamento de eventos \_ \_ \_ \_ \_ e/s de arquivo de disco", "sinalizador de rastreamento de eventos, e/s de disco", "Dispatcher de sinalizador de rastreamento de eventos", "falha de página de sinalizador de rastreamento de eventos", \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ registro de sinalizador de rastreamento de evento "," \_ sinalizador de rastreamento de evento \_ \_ ALPC "," sinalizador de rastreamento de eventos \_ \_ \_ dividir \_ e/s "," \_ Driver de sinalizador de rastreamento de eventos " \_ \_ ," \_ \_ \_ perfil de sinalizador de rastreamento de eventos "," \_ \_ \_ \_ e/s de arquivo de sinalizador de rastreamento de eventos ", \_ \_ Flag \_ File \_ Io \_ init"}**, **ValueMap {"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100" , "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span><span class="sxs-lookup"><span data-stu-id="0fb9a-116">Qualifiers: **DefineValues{"EVENT\_TRACE\_FLAG\_PROCESS", "EVENT\_TRACE\_FLAG\_THREAD", "EVENT\_TRACE\_FLAG\_IMAGE\_LOAD", "EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS", "EVENT\_TRACE\_FLAG\_CSWITCH", "EVENT\_TRACE\_FLAG\_DPC", "EVENT\_TRACE\_FLAG\_INTERRUPT", "EVENT\_TRACE\_FLAG\_SYSTEMCALL", "EVENT\_TRACE\_FLAG\_DISK\_IO", "EVENT\_TRACE\_FLAG\_DISK\_FILE\_IO", "EVENT\_TRACE\_FLAG\_DISK\_IO\_INIT", "EVENT\_TRACE\_FLAG\_DISPATCHER", "EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS", "EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS", "EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC", "EVENT\_TRACE\_FLAG\_NETWORK\_TCPIP", "EVENT\_TRACE\_FLAG\_REGISTRY", "EVENT\_TRACE\_FLAG\_ALPC", "EVENT\_TRACE\_FLAG\_SPLIT\_IO", "EVENT\_TRACE\_FLAG\_DRIVER", "EVENT\_TRACE\_FLAG\_PROFILE", "EVENT\_TRACE\_FLAG\_FILE\_IO", "EVENT\_TRACE\_FLAG\_FILE\_IO\_INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**</span></span>
</dt> </dl>

<span data-ttu-id="0fb9a-117">Habilite o sinalizador que indica os provedores de kernel habilitados.</span><span class="sxs-lookup"><span data-stu-id="0fb9a-117">Enable flag that indicates the enabled kernel providers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0fb9a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fb9a-118">Requirements</span></span>



| <span data-ttu-id="0fb9a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fb9a-119">Requirement</span></span> | <span data-ttu-id="0fb9a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0fb9a-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0fb9a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fb9a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb9a-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0fb9a-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0fb9a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fb9a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb9a-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0fb9a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 




