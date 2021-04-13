---
description: Essa classe é a classe de tipo de evento para eventos de e/s de disco. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: fe7d4efa-3d39-4438-a1a6-af3f65ea3deb
title: Classe DiskIo_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup1
- DiskIo_TypeGroup1.DiskNumber
- DiskIo_TypeGroup1.IrpFlags
- DiskIo_TypeGroup1.TransferSize
- DiskIo_TypeGroup1.Reserved
- DiskIo_TypeGroup1.ByteOffset
- DiskIo_TypeGroup1.FileObject
- DiskIo_TypeGroup1.Irp
- DiskIo_TypeGroup1.HighResResponseTime
- DiskIo_TypeGroup1.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d20f80eb840283600f5d106f89c6cf8032ee746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501927"
---
# <a name="diskio_typegroup1-class"></a><span data-ttu-id="be404-104">\_Classe DiskIo TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="be404-104">DiskIo\_TypeGroup1 class</span></span>

<span data-ttu-id="be404-105">Essa classe é a classe de tipo de evento para eventos de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="be404-105">This class is the event type class for disk I/O events.</span></span>

<span data-ttu-id="be404-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="be404-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="be404-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be404-107">Syntax</span></span>

``` syntax
[EventType{10,11}, EventTypeName{"Read","Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
  uint32 DiskNumber;
  uint32 IrpFlags;
  uint32 TransferSize;
  uint32 Reserved;
  sint64 ByteOffset;
  uint32 FileObject;
  uint32 Irp;
  uint64 HighResResponseTime;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="be404-108">Membros</span><span class="sxs-lookup"><span data-stu-id="be404-108">Members</span></span>

<span data-ttu-id="be404-109">A classe **DiskIo \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="be404-109">The **DiskIo\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="be404-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="be404-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be404-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="be404-111">Properties</span></span>

<span data-ttu-id="be404-112">A classe **DiskIo \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="be404-112">The **DiskIo\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be404-113">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="be404-113">**ByteOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-114">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="be404-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="be404-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-116">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="be404-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="be404-117">Deslocamento de bytes do início do disco físico.</span><span class="sxs-lookup"><span data-stu-id="be404-117">Byte offset from the beginning of the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="be404-118">**DiskNumber**</span><span class="sxs-lookup"><span data-stu-id="be404-118">**DiskNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be404-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be404-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-121">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="be404-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="be404-122">Número que identifica o disco físico.</span><span class="sxs-lookup"><span data-stu-id="be404-122">Number that identifies the physical disk.</span></span>

</dd> <dt>

<span data-ttu-id="be404-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="be404-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be404-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be404-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-126">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**ponteiro**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="be404-126">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="be404-127">Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**de \_ nome de FileIo**](fileio-name.md) para determinar o arquivo envolvido na operação de e/s.</span><span class="sxs-lookup"><span data-stu-id="be404-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the file involved in the I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="be404-128">**HighResResponseTime**</span><span class="sxs-lookup"><span data-stu-id="be404-128">**HighResResponseTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-129">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be404-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be404-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-131">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span><span class="sxs-lookup"><span data-stu-id="be404-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)</span></span>
</dt> </dl>

<span data-ttu-id="be404-132">O tempo entre o início e a conclusão de e/s conforme medido pelo Gerenciador de partições (nas unidades de tique [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).</span><span class="sxs-lookup"><span data-stu-id="be404-132">The time between I/O initiation and completion as measured by the partition manager (in the [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) tick units).</span></span>

<span data-ttu-id="be404-133">**Windows Server 2003:** Essa propriedade tem um valor de [**WmiDataId**](event-tracing-mof-qualifiers.md) de 7.</span><span class="sxs-lookup"><span data-stu-id="be404-133">**Windows Server 2003:** This property has a [**WmiDataId**](event-tracing-mof-qualifiers.md) value of 7.</span></span>

<span data-ttu-id="be404-134">**Windows 2000 Server e windows 2000 Professional:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="be404-134">**Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="be404-135">**IRP**</span><span class="sxs-lookup"><span data-stu-id="be404-135">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-136">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be404-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be404-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-138">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**ponteiro**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="be404-138">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="be404-139">O pacote de solicitação de e/s, que identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="be404-139">The I/O request packet, which identifies the I/O activity.</span></span>

<span data-ttu-id="be404-140">**Windows server 2003, windows 2000 Server e windows 2000 Professional:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="be404-140">**Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="be404-141">**IrpFlags**</span><span class="sxs-lookup"><span data-stu-id="be404-141">**IrpFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be404-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be404-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-144">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**formato**](event-tracing-mof-qualifiers.md) ("x")</span><span class="sxs-lookup"><span data-stu-id="be404-144">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**Format**](event-tracing-mof-qualifiers.md) ("x")</span></span>
</dt> </dl>

<span data-ttu-id="be404-145">Pode conter um ou mais dos seguintes sinalizadores de pacotes de solicitação de e/s (definidos em Ntddk. h, que é um arquivo de cabeçalho do DDK):</span><span class="sxs-lookup"><span data-stu-id="be404-145">Can contain one or more of the following I/O request packet flags (defined in Ntddk.h, which is a DDK header file):</span></span>

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 <span data-ttu-id="be404-146">**IRP \_ NOcache**</span><span class="sxs-lookup"><span data-stu-id="be404-146">**IRP\_NOCACHE**</span></span>
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 <span data-ttu-id="be404-147">**\_ \_ e/s de paginação IRP**</span><span class="sxs-lookup"><span data-stu-id="be404-147">**IRP\_PAGING\_IO**</span></span>
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 <span data-ttu-id="be404-148">**\_conclusão de montagem de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-148">**IRP\_MOUNT\_COMPLETION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 <span data-ttu-id="be404-149">**\_API SÍNCRONA \_ IRP**</span><span class="sxs-lookup"><span data-stu-id="be404-149">**IRP\_SYNCHRONOUS\_API**</span></span>
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 <span data-ttu-id="be404-150">**\_IRP associado a IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-150">**IRP\_ASSOCIATED\_IRP**</span></span>
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 <span data-ttu-id="be404-151">**\_e/s em buffer de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-151">**IRP\_BUFFERED\_IO**</span></span>
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

<span data-ttu-id="be404-152">**\_buffer de DESalocação de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-152">**IRP\_DEALLOCATE\_BUFFER**</span></span>
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 <span data-ttu-id="be404-153">**\_operação de entrada de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-153">**IRP\_INPUT\_OPERATION**</span></span>
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 <span data-ttu-id="be404-154">**\_ \_ e/s de paginação síncrona IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-154">**IRP\_SYNCHRONOUS\_PAGING\_IO**</span></span>
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 <span data-ttu-id="be404-155">**\_operação de criação de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-155">**IRP\_CREATE\_OPERATION**</span></span>
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

<span data-ttu-id="be404-156">**\_operação de leitura de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-156">**IRP\_READ\_OPERATION**</span></span>
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 <span data-ttu-id="be404-157">**\_operação de gravação de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-157">**IRP\_WRITE\_OPERATION**</span></span>
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 <span data-ttu-id="be404-158">**\_operação de fechamento de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-158">**IRP\_CLOSE\_OPERATION**</span></span>
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 <span data-ttu-id="be404-159">**\_conclusão de \_ e/s de adiamento de IRP \_**</span><span class="sxs-lookup"><span data-stu-id="be404-159">**IRP\_DEFER\_IO\_COMPLETION**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="be404-160">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="be404-160">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-161">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be404-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be404-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-163">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span><span class="sxs-lookup"><span data-stu-id="be404-163">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)</span></span>
</dt> </dl>

<span data-ttu-id="be404-164">O identificador do thread emissor.</span><span class="sxs-lookup"><span data-stu-id="be404-164">The identifier of the issuing thread.</span></span>

<span data-ttu-id="be404-165">**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 com SP1, Windows server 2003, windows 2000 Server e windows 2000 Professional:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="be404-165">**Windows Server 2008 R2, Windows Server 2008, Windows 7, Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="be404-166">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="be404-166">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be404-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be404-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-169">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="be404-169">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="be404-170">Reservado.</span><span class="sxs-lookup"><span data-stu-id="be404-170">Reserved.</span></span>

<span data-ttu-id="be404-171">**Windows server 2008 R2, Windows server 2008 e Windows 7:** O nome da propriedade é **QueueDepth**, que contém a contagem de tiques da CPU desde o início da operação até o fim da operação.</span><span class="sxs-lookup"><span data-stu-id="be404-171">**Windows Server 2008 R2, Windows Server 2008 and Windows 7:** The name of the property is **QueueDepth**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="be404-172">Observe que esse valor pode ser estourado.</span><span class="sxs-lookup"><span data-stu-id="be404-172">Note that this value can overflow.</span></span>

<span data-ttu-id="be404-173">**Windows Vista, Windows server 2003 com SP1, Windows Server 2003, windows 2000 Server e windows 2000 Professional:** O nome da propriedade é **ResponseTime**, que contém a contagem de tiques da CPU desde o início da operação até o fim da operação.</span><span class="sxs-lookup"><span data-stu-id="be404-173">**Windows Vista, Windows Server 2003 with SP1, Windows Server 2003, Windows 2000 Server and Windows 2000 Professional:** The name of the property is **ResponseTime**, which contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="be404-174">Observe que esse valor pode ser estourado.</span><span class="sxs-lookup"><span data-stu-id="be404-174">Note that this value can overflow.</span></span>

</dd> <dt>

<span data-ttu-id="be404-175">**Transferências**</span><span class="sxs-lookup"><span data-stu-id="be404-175">**TransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be404-176">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be404-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be404-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="be404-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be404-178">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="be404-178">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="be404-179">Tamanho dos dados lidos ou gravados do disco, em bytes.</span><span class="sxs-lookup"><span data-stu-id="be404-179">Size of data read to or written from disk, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be404-180">Comentários</span><span class="sxs-lookup"><span data-stu-id="be404-180">Remarks</span></span>

<span data-ttu-id="be404-181">O Windows Server 2003 usa a seguinte definição para a classe de tipo de evento **DiskIo \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="be404-181">Windows Server 2003 uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), read] uint64 HighResResponseTime;
};
```

<span data-ttu-id="be404-182">A propriedade **ResponseTime** contém a contagem de tiques da CPU desde o início da operação até o fim da operação.</span><span class="sxs-lookup"><span data-stu-id="be404-182">The **ResponseTime** property contains the CPU tick count from the beginning of the operation to the end of the operation.</span></span> <span data-ttu-id="be404-183">Observe que esse valor pode ser estourado.</span><span class="sxs-lookup"><span data-stu-id="be404-183">Note that this value can overflow.</span></span>

<span data-ttu-id="be404-184">Não há suporte para a propriedade **HighResResponseTime** .</span><span class="sxs-lookup"><span data-stu-id="be404-184">The **HighResResponseTime** property is not supported.</span></span>

<span data-ttu-id="be404-185">O Windows Server 2003 com SP1 e o Windows Vista usa a seguinte definição para a classe de tipo de evento **DiskIo \_ TypeGroup1** .</span><span class="sxs-lookup"><span data-stu-id="be404-185">Windows Server 2003 with SP1 and Windows Vista uses the following definition for the **DiskIo\_TypeGroup1** event type class.</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Read", "Write"}]
class DiskIo_TypeGroup1 : DiskIo
{
    [WmiDataId(1), read] uint32 DiskNumber;
    [WmiDataId(2), format("x"), read] uint32 IrpFlags;
    [WmiDataId(3), read] uint32 TransferSize;
    [WmiDataId(4), read] uint32 ResponseTime;
    [WmiDataId(5), read] uint64 ByteOffset;
    [WmiDataId(6), pointer, read] uint32 FileObject;
    [WmiDataId(7), pointer, read] uint32 Irp;
    [WmiDataId(8), read] uint64 HighResResponseTime;
};
```

<span data-ttu-id="be404-186">A propriedade **IRP** é o pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="be404-186">The **Irp** property is the I/O request packet.</span></span> <span data-ttu-id="be404-187">Essa propriedade identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="be404-187">This property identifies the I/O activity.</span></span> <span data-ttu-id="be404-188">Você pode usar essa propriedade com os eventos [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) para correlacionar o tempo de resposta.</span><span class="sxs-lookup"><span data-stu-id="be404-188">You can use this property with the [**DiskIo\_TypeGroup2**](diskio-typegroup2.md) events to correlate response time.</span></span>

<span data-ttu-id="be404-189">Há suporte para a propriedade **HighResResponseTime** .</span><span class="sxs-lookup"><span data-stu-id="be404-189">The **HighResResponseTime** property is supported.</span></span> <span data-ttu-id="be404-190">A propriedade contém o tempo entre o início e a conclusão de e/s, conforme medido por PartitionManager (nas unidades KeQueryPerformanceCounter).</span><span class="sxs-lookup"><span data-stu-id="be404-190">The property contains the time between I/O initiation and completion as measured by PartitionManager (in the KeQueryPerformanceCounter units).</span></span> <span data-ttu-id="be404-191">Use essa propriedade em vez da propriedade **ResponseTime** para determinar o tempo de resposta de e/s do disco.</span><span class="sxs-lookup"><span data-stu-id="be404-191">Use this property instead of the **ResponseTime** property to determine the disk I/O response time.</span></span>

## <a name="requirements"></a><span data-ttu-id="be404-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be404-192">Requirements</span></span>



| <span data-ttu-id="be404-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="be404-193">Requirement</span></span> | <span data-ttu-id="be404-194">Valor</span><span class="sxs-lookup"><span data-stu-id="be404-194">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="be404-195">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be404-195">Minimum supported client</span></span><br/> | <span data-ttu-id="be404-196">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="be404-196">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="be404-197">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be404-197">Minimum supported server</span></span><br/> | <span data-ttu-id="be404-198">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="be404-198">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="be404-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="be404-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be404-200">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="be404-200">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 
