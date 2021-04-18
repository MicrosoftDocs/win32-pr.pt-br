---
title: Tipo complexo FilterListType
description: Define uma lista de filtros que um controlador ETW pode passar para seu provedor para limitar ainda mais os eventos que ele grava.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Log de eventos do tipo complexo FilterListType
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295891"
---
# <a name="filterlisttype-complex-type"></a><span data-ttu-id="e8529-104">Tipo complexo FilterListType</span><span class="sxs-lookup"><span data-stu-id="e8529-104">FilterListType Complex Type</span></span>

<span data-ttu-id="e8529-105">Define uma lista de filtros que um controlador ETW pode passar para seu provedor para limitar ainda mais os eventos que ele grava.</span><span class="sxs-lookup"><span data-stu-id="e8529-105">Defines a list of filters that an ETW controller can pass to your provider to further limit the events that it writes.</span></span>

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e8529-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e8529-106">Child elements</span></span>



| <span data-ttu-id="e8529-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e8529-107">Element</span></span>    | <span data-ttu-id="e8529-108">Type</span><span class="sxs-lookup"><span data-stu-id="e8529-108">Type</span></span>                                                             | <span data-ttu-id="e8529-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8529-109">Description</span></span>                   |
|------------|------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="e8529-110">**filter**</span><span class="sxs-lookup"><span data-stu-id="e8529-110">**filter**</span></span> | [<span data-ttu-id="e8529-111">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="e8529-111">**FilterType**</span></span>](eventmanifestschema-filtertype-complextype.md) | <span data-ttu-id="e8529-112">Uma lista de filtros.</span><span class="sxs-lookup"><span data-stu-id="e8529-112">A list of filters.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e8529-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8529-113">Remarks</span></span>

<span data-ttu-id="e8529-114">Um controlador ETW é um aplicativo que chama a função [**StartTrace**](/windows/desktop/ETW/starttrace) para criar uma sessão de ETW.</span><span class="sxs-lookup"><span data-stu-id="e8529-114">An ETW controller is an application that calls the [**StartTrace**](/windows/desktop/ETW/starttrace) function to create an ETW session.</span></span> <span data-ttu-id="e8529-115">Para obter detalhes, consulte [controlando sessões de rastreamento de eventos](/windows/desktop/ETW/controlling-event-tracing-sessions).</span><span class="sxs-lookup"><span data-stu-id="e8529-115">For details, see [Controlling Event Tracing Sessions](/windows/desktop/ETW/controlling-event-tracing-sessions).</span></span> <span data-ttu-id="e8529-116">O controlador pode usar a função [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) para enumerar os filtros que você definir.</span><span class="sxs-lookup"><span data-stu-id="e8529-116">The controller can use the [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) function to enumerate the filters that you define.</span></span> <span data-ttu-id="e8529-117">Em seguida, o controlador pode passar um ou mais dos filtros ao chamar a função [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) para habilitar seu provedor.</span><span class="sxs-lookup"><span data-stu-id="e8529-117">The controller can then pass one or more of the filters when it calls the [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) function to enable your provider.</span></span> <span data-ttu-id="e8529-118">Seu provedor recebe os filtros, juntamente com o restante dos parâmetros de habilitação, em sua função de retorno de chamada do [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .</span><span class="sxs-lookup"><span data-stu-id="e8529-118">Your provider receives the filters, along with the rest of the enable parameters, in your [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8529-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8529-119">Requirements</span></span>



| <span data-ttu-id="e8529-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8529-120">Requirement</span></span> | <span data-ttu-id="e8529-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e8529-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e8529-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8529-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8529-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e8529-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e8529-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8529-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8529-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="e8529-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

