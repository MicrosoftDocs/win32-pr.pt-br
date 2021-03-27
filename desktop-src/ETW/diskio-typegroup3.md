---
description: Essa classe é a classe de tipo de evento para eventos de liberação de e/s de disco. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f
title: Classe DiskIo_TypeGroup3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup3
- DiskIo_TypeGroup3.DiskNumber
- DiskIo_TypeGroup3.IrpFlags
- DiskIo_TypeGroup3.HighResResponseTime
- DiskIo_TypeGroup3.Irp
- DiskIo_TypeGroup3.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63ca227269dab249be755da22288ce41696a19e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967299"
---
# <a name="diskio_typegroup3-class"></a><span data-ttu-id="c5524-104">\_Classe DiskIo TypeGroup3</span><span class="sxs-lookup"><span data-stu-id="c5524-104">DiskIo\_TypeGroup3 class</span></span>

<span data-ttu-id="c5524-105">Essa classe é a classe de tipo de evento para eventos de liberação de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="c5524-105">This class is the event type class for disk I/O flush events.</span></span>

<span data-ttu-id="c5524-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c5524-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5524-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5524-107">Syntax</span></span>

``` syntax
[EventType{14}, EventTypeName{"FlushBuffers"}]
class DiskIo_TypeGroup3 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint64 HighResResponseTime;
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="c5524-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c5524-108">Members</span></span>

<span data-ttu-id="c5524-109">A classe **DiskIo \_ TypeGroup3** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c5524-109">The **DiskIo\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="c5524-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5524-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5524-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5524-111">Properties</span></span>

<span data-ttu-id="c5524-112">A classe **DiskIo \_ TypeGroup3** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c5524-112">The **DiskIo\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5524-113">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="c5524-113">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5524-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5524-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5524-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5524-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5524-116">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="c5524-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c5524-117">Número que identifica o disco físico.</span><span class="sxs-lookup"><span data-stu-id="c5524-117">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="c5524-118">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="c5524-118">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5524-119">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c5524-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c5524-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5524-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5524-121">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="c5524-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="c5524-122">Contagem de tiques de CPU desde o início da operação até o fim da operação.</span><span class="sxs-lookup"><span data-stu-id="c5524-122">CPU tick count from the beginning of the operation to the end of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5524-123">**IRP**</span><span class="sxs-lookup"><span data-stu-id="c5524-123">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5524-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5524-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5524-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5524-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5524-126">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**ponteiro**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="c5524-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="c5524-127">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="c5524-127">I/O request packet.</span></span> <span data-ttu-id="c5524-128">Essa propriedade identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="c5524-128">This property identifies the I/O activity.</span></span>

</dd> <dt>

<span data-ttu-id="c5524-129">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="c5524-129">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5524-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5524-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5524-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5524-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5524-132">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**formato**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="c5524-132">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="c5524-133">Pode conter um ou mais dos seguintes sinalizadores de pacotes de solicitação de e/s (definidos em Ntddk. h, que é um arquivo de cabeçalho do DDK):</span><span class="sxs-lookup"><span data-stu-id="c5524-133">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="c5524-134">**IRP \_ NOcache**</span><span class="sxs-lookup"><span data-stu-id="c5524-134">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="c5524-135">**\_ \_ e/s de paginação IRP**</span><span class="sxs-lookup"><span data-stu-id="c5524-135">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="c5524-136">**\_conclusão de montagem de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-136">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="c5524-137">**\_API SÍNCRONA \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="c5524-137">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="c5524-138">**\_IRP associado a IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-138">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="c5524-139">**\_e/s em buffer de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-139">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="c5524-140">**\_buffer de DESalocação de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-140">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="c5524-141">**\_operação de entrada de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-141">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="c5524-142">**\_ \_ e/s de paginação síncrona IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-142">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="c5524-143">**\_operação de criação de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-143">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="c5524-144">**\_operação de leitura de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-144">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="c5524-145">**\_operação de gravação de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-145">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="c5524-146">**\_operação de fechamento de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-146">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="c5524-147">**\_conclusão de \_ e/s de adiamento de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="c5524-147">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c5524-148">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="c5524-148">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5524-149">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5524-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c5524-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c5524-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5524-151">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="c5524-151">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="c5524-152">O identificador do thread emissor.</span><span class="sxs-lookup"><span data-stu-id="c5524-152">The identifier of the issuing thread.</span></span>

<span data-ttu-id="c5524-153">**Windows server 2008 R2, Windows server 2008, Windows 7 e Windows Vista:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c5524-153">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5524-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5524-154">Requirements</span></span>



| <span data-ttu-id="c5524-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5524-155">Requirement</span></span> | <span data-ttu-id="c5524-156">Valor</span><span class="sxs-lookup"><span data-stu-id="c5524-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c5524-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5524-157">Minimum supported client</span></span><br/> | <span data-ttu-id="c5524-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5524-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c5524-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5524-159">Minimum supported server</span></span><br/> | <span data-ttu-id="c5524-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5524-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5524-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5524-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5524-162">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="c5524-162">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




