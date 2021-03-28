---
description: Essa classe é a classe de tipo de evento para os eventos de retorno de chamada de função principal do driver. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: Classe DriverMajorFunctionReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21340224253d1eb3f3ddc733bf2d43e847844282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501388"
---
# <a name="drivermajorfunctionreturn-class"></a><span data-ttu-id="c9776-104">Classe DriverMajorFunctionReturn</span><span class="sxs-lookup"><span data-stu-id="c9776-104">DriverMajorFunctionReturn class</span></span>

<span data-ttu-id="c9776-105">Essa classe é a classe de tipo de evento para os eventos de retorno de chamada de função principal do driver.</span><span class="sxs-lookup"><span data-stu-id="c9776-105">This class is the event type class for driver major function call return events.</span></span>

<span data-ttu-id="c9776-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c9776-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9776-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9776-107">Syntax</span></span>

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="c9776-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c9776-108">Members</span></span>

<span data-ttu-id="c9776-109">A classe **DriverMajorFunctionReturn** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c9776-109">The **DriverMajorFunctionReturn** class has these types of members:</span></span>

-   [<span data-ttu-id="c9776-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9776-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9776-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9776-111">Properties</span></span>

<span data-ttu-id="c9776-112">A classe **DriverMajorFunctionReturn** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c9776-112">The **DriverMajorFunctionReturn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9776-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="c9776-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9776-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9776-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9776-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9776-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9776-116">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="c9776-116">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c9776-117">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="c9776-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="c9776-118">**UniqMatchId**</span><span class="sxs-lookup"><span data-stu-id="c9776-118">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9776-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9776-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9776-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9776-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9776-121">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="c9776-121">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="c9776-122">Identificador que identifica a solicitação de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="c9776-122">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="c9776-123">Use esse identificador para correlacionar com os outros eventos de driver, por exemplo, o evento [**DriverCompleteRequest**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="c9776-123">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9776-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9776-124">Requirements</span></span>



| <span data-ttu-id="c9776-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9776-125">Requirement</span></span> | <span data-ttu-id="c9776-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c9776-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9776-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9776-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c9776-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9776-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9776-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9776-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c9776-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9776-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9776-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9776-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9776-132">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="c9776-132">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




