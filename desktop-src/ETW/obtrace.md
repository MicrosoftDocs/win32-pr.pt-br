---
description: Representa a classe pai da qual todas as classes de rastreamento de eventos do Gerenciador de objetos são derivadas.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Classe ObTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: ca89f58df9f5dd741da5b1fb8572b153c956cd43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662542"
---
# <a name="obtrace-class"></a><span data-ttu-id="1d390-103">Classe ObTrace</span><span class="sxs-lookup"><span data-stu-id="1d390-103">ObTrace class</span></span>

<span data-ttu-id="1d390-104">Representa a classe pai da qual todas as classes de rastreamento de eventos do Gerenciador de objetos são derivadas.</span><span class="sxs-lookup"><span data-stu-id="1d390-104">Represents the parent class from which all object manager event trace classes are derived.</span></span>

<span data-ttu-id="1d390-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1d390-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d390-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d390-106">Syntax</span></span>

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1d390-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1d390-107">Members</span></span>

<span data-ttu-id="1d390-108">A classe **ObTrace** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="1d390-108">The **ObTrace** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d390-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d390-109">Remarks</span></span>

<span data-ttu-id="1d390-110">Para habilitar o rastreamento de eventos do Gerenciador de objetos, chame a função [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) com o parâmetro *InformationClass* igual ao valor de enumeração de [**classe de \_ informações \_ de rastreamento**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** e o membro **EnableFlags** da estrutura de [**\_ \_ Propriedades do rastreamento de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) igual ao **\_ \_ identificador de OB perf** (0x80000040).</span><span class="sxs-lookup"><span data-stu-id="1d390-110">To enable object manager event tracing, call the [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) function with the *InformationClass* parameter equal to the [**TRACE\_INFO\_CLASS**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) enumeration value **TraceSystemTraceEnableFlagsInfo** and the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure's **EnableFlags** member equal to **PERF\_OB\_HANDLE** (0x80000040).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d390-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d390-111">Requirements</span></span>



| <span data-ttu-id="1d390-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d390-112">Requirement</span></span> | <span data-ttu-id="1d390-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1d390-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d390-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d390-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1d390-115">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1d390-115">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1d390-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d390-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1d390-117">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1d390-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1d390-118">MOF</span><span class="sxs-lookup"><span data-stu-id="1d390-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d390-119"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d390-119"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 
