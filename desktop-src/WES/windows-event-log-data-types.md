---
title: Tipos de dados de log de eventos do Windows (WinEvt. h)
description: O log de eventos do Windows define os seguintes tipos de dados
ms.assetid: 1aad25fe-7503-4ef8-a40a-63457bd9a007
keywords:
- EVT_HANDLE
- PEVT_HANDLE
- EVT_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a93794d8cc3a254fe182c439698324dccdfc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644621"
---
# <a name="windows-event-log-data-types"></a><span data-ttu-id="74f73-106">Tipos de dados de log de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="74f73-106">Windows Event Log Data Types</span></span>

<span data-ttu-id="74f73-107">O log de eventos do Windows define os seguintes tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="74f73-107">Windows Event Log defines the following data types:</span></span>


```C++
typedef HANDLE EVT_HANDLE;
typedef HANDLE* PEVT_HANDLE;
typedef HANDLE EVT_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="74f73-108">**\_alça EVT**</span><span class="sxs-lookup"><span data-stu-id="74f73-108">**EVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="74f73-109">Um identificador para um objeto de log de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="74f73-109">A handle to a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="74f73-110">**identificador de PEVT \_**</span><span class="sxs-lookup"><span data-stu-id="74f73-110">**PEVT\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="74f73-111">Um ponteiro para o identificador de um objeto de log de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="74f73-111">A pointer to the handle of a Windows Event Log object.</span></span>

</dd> <dt>

<span data-ttu-id="74f73-112">**\_identificador da \_ propriedade da matriz de objetos EVT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="74f73-112">**EVT\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="74f73-113">Um identificador para uma matriz de objetos de log de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="74f73-113">A handle to an array of Windows Event Log objects.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74f73-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74f73-114">Requirements</span></span>



| <span data-ttu-id="74f73-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="74f73-115">Requirement</span></span> | <span data-ttu-id="74f73-116">Valor</span><span class="sxs-lookup"><span data-stu-id="74f73-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74f73-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74f73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="74f73-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74f73-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="74f73-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74f73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="74f73-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74f73-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74f73-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74f73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f73-122"><dt>WinEvt. h</dt></span><span class="sxs-lookup"><span data-stu-id="74f73-122"><dt>WinEvt.h</dt></span></span> </dl> |



 

 





