---
description: Essa classe é a classe de tipo de evento para eventos de término de operação de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 3925d5bf-f412-4248-a61f-e667efa9debd
title: Classe FileIo_OpEnd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_OpEnd
- FileIo_OpEnd.IrpPtr
- FileIo_OpEnd.ExtraInfo
- FileIo_OpEnd.NtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3f1c495cf44b84f8d7661b40cadec6ea255c6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662798"
---
# <a name="fileio_opend-class"></a><span data-ttu-id="e80b0-104">\_Classe aberta de FileIo</span><span class="sxs-lookup"><span data-stu-id="e80b0-104">FileIo\_OpEnd class</span></span>

<span data-ttu-id="e80b0-105">Essa classe é a classe de tipo de evento para eventos de término de operação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e80b0-105">This class is the event type class for file operation end events.</span></span>

<span data-ttu-id="e80b0-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="e80b0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80b0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e80b0-107">Syntax</span></span>

``` syntax
[EventType{76}, EventTypeName{"OperationEnd"}]
class FileIo_OpEnd : FileIo
{
  uint32 IrpPtr;
  uint32 ExtraInfo;
  uint32 NtStatus;
};
```

## <a name="members"></a><span data-ttu-id="e80b0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e80b0-108">Members</span></span>

<span data-ttu-id="e80b0-109">A **classe \_ aberta FileIo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e80b0-109">The **FileIo\_OpEnd** class has these types of members:</span></span>

-   [<span data-ttu-id="e80b0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e80b0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e80b0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e80b0-111">Properties</span></span>

<span data-ttu-id="e80b0-112">A **classe \_ aberta FileIo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e80b0-112">The **FileIo\_OpEnd** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e80b0-113">**ExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="e80b0-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e80b0-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e80b0-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e80b0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e80b0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e80b0-116">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="e80b0-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e80b0-117">Informações extras retornadas pelo sistema de arquivos para a operação.</span><span class="sxs-lookup"><span data-stu-id="e80b0-117">Extra information returned by the file system for the operation.</span></span> <span data-ttu-id="e80b0-118">Por exemplo, para uma solicitação de leitura, o número real de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="e80b0-118">For example for a read request, the actual number of bytes that were read.</span></span>

</dd> <dt>

<span data-ttu-id="e80b0-119">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="e80b0-119">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e80b0-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e80b0-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e80b0-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e80b0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e80b0-122">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="e80b0-122">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="e80b0-123">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="e80b0-123">IO request packet.</span></span> <span data-ttu-id="e80b0-124">Essa propriedade identifica a atividade de e/s que está terminando.</span><span class="sxs-lookup"><span data-stu-id="e80b0-124">This property identifies the IO activity that is ending.</span></span>

</dd> <dt>

<span data-ttu-id="e80b0-125">**NtStatus**</span><span class="sxs-lookup"><span data-stu-id="e80b0-125">**NtStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e80b0-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e80b0-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e80b0-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e80b0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e80b0-128">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="e80b0-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="e80b0-129">Valor de retorno da operação.</span><span class="sxs-lookup"><span data-stu-id="e80b0-129">Return value from the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e80b0-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e80b0-130">Remarks</span></span>

<span data-ttu-id="e80b0-131">Os eventos de [**FileIo**](fileio.md) são registrados no início da operação.</span><span class="sxs-lookup"><span data-stu-id="e80b0-131">[**FileIo**](fileio.md) events are logged at the beginning of the operation.</span></span> <span data-ttu-id="e80b0-132">Os eventos abertos podem ser habilitados separadamente para indicar o fim dessas operações.</span><span class="sxs-lookup"><span data-stu-id="e80b0-132">OpEnd events can be enabled separately to indicate the end of those operations.</span></span> <span data-ttu-id="e80b0-133">O IRP pode ser usado para correlacionar os eventos de início e término.</span><span class="sxs-lookup"><span data-stu-id="e80b0-133">Irp can be used to correlate the begin and end events.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80b0-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e80b0-134">Requirements</span></span>



| <span data-ttu-id="e80b0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80b0-135">Requirement</span></span> | <span data-ttu-id="e80b0-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e80b0-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e80b0-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e80b0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e80b0-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e80b0-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e80b0-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e80b0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e80b0-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e80b0-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e80b0-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e80b0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80b0-142">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="e80b0-142">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




