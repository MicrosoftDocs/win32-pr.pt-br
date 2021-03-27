---
description: Essa classe é a classe de tipo de evento para eventos de retorno de solicitação de conclusão de driver. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 04505f8c-a11e-4bf7-91c0-fca1b5846d80
title: Classe DriverCompleteRequestReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequestReturn
- DriverCompleteRequestReturn.Irp
- DriverCompleteRequestReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c147573578e067b7fb1b588545a1d9f231e35f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501390"
---
# <a name="drivercompleterequestreturn-class"></a><span data-ttu-id="883c6-104">Classe DriverCompleteRequestReturn</span><span class="sxs-lookup"><span data-stu-id="883c6-104">DriverCompleteRequestReturn class</span></span>

<span data-ttu-id="883c6-105">Essa classe é a classe de tipo de evento para eventos de retorno de solicitação de conclusão de driver.</span><span class="sxs-lookup"><span data-stu-id="883c6-105">This class is the event type class for driver complete request return events.</span></span>

<span data-ttu-id="883c6-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="883c6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="883c6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="883c6-107">Syntax</span></span>

``` syntax
[EventType{53}, EventTypeName{"DrvComplReqRet"}]
class DriverCompleteRequestReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="883c6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="883c6-108">Members</span></span>

<span data-ttu-id="883c6-109">A classe **DriverCompleteRequestReturn** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="883c6-109">The **DriverCompleteRequestReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="883c6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="883c6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="883c6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="883c6-111">Properties</span></span>

<span data-ttu-id="883c6-112">A classe **DriverCompleteRequestReturn** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="883c6-112">The **DriverCompleteRequestReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="883c6-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="883c6-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="883c6-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="883c6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="883c6-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="883c6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="883c6-116">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="883c6-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="883c6-117">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="883c6-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="883c6-118">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="883c6-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="883c6-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="883c6-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="883c6-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="883c6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="883c6-121">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="883c6-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="883c6-122">Identificador que identifica a solicitação de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="883c6-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="883c6-123">Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, o evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="883c6-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="883c6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="883c6-124">Requirements</span></span>



| <span data-ttu-id="883c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="883c6-125">Requirement</span></span> | <span data-ttu-id="883c6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="883c6-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="883c6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="883c6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="883c6-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="883c6-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="883c6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="883c6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="883c6-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="883c6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="883c6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="883c6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883c6-132">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="883c6-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




