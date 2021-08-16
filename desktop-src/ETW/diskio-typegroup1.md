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
ms.openlocfilehash: 3a69643602a59fa7be8cd844f3f2908c92e2e08545f7444d1002ec1542b36730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814972"
---
# <a name="diskio_typegroup1-class"></a>\_Classe DiskIo TypeGroup1

Essa classe é a classe de tipo de evento para eventos de e/s de disco.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe **DiskIo \_ TypeGroup1** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **DiskIo \_ TypeGroup1** tem essas propriedades.

<dl> <dt>

**ByteOffset**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)
</dt> </dl>

Deslocamento de bytes do início do disco físico.

</dd> <dt>

**DiskNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)
</dt> </dl>

Número que identifica o disco físico.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (6), [**ponteiro**](event-tracing-mof-qualifiers.md)
</dt> </dl>

Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**de \_ nome de FileIo**](fileio-name.md) para determinar o arquivo envolvido na operação de e/s.

</dd> <dt>

**HighResResponseTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (8)
</dt> </dl>

O tempo entre o início e a conclusão de e/s conforme medido pelo Gerenciador de partições (nas unidades de tique [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-kequeryperformancecounter) ).

**Windows Server 2003:** Essa propriedade tem um valor de [**WmiDataId**](event-tracing-mof-qualifiers.md) de 7.

**Windows servidor 2000 e Windows 2000 Professional:** Não há suporte para essa propriedade.

</dd> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (7), [**ponteiro**](event-tracing-mof-qualifiers.md)
</dt> </dl>

O pacote de solicitação de e/s, que identifica a atividade de e/s.

**Windows server 2003, Windows 2000 server e Windows 2000 Professional:** Não há suporte para essa propriedade.

</dd> <dt>

**IrpFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2), [**formato**](event-tracing-mof-qualifiers.md) ("x")
</dt> </dl>

Pode conter um ou mais dos seguintes sinalizadores de pacotes de solicitação de e/s (definidos em Ntddk. h, que é um arquivo de cabeçalho do DDK):

<dl><span id="__IRP_NOCACHE"></span><span id="__irp_nocache"></span><dt>

 **IRP \_ NOcache**
</dt><span id="__IRP_PAGING_IO"></span><span id="__irp_paging_io"></span><dt>

 **\_ \_ e/s de paginação IRP**
</dt><span id="__IRP_MOUNT_COMPLETION"></span><span id="__irp_mount_completion"></span><dt>

 **\_conclusão de montagem de IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_API"></span><span id="__irp_synchronous_api"></span><dt>

 **\_API SÍNCRONA \_ IRP**
</dt><span id="__IRP_ASSOCIATED_IRP"></span><span id="__irp_associated_irp"></span><dt>

 **\_IRP associado a IRP \_**
</dt><span id="__IRP_BUFFERED_IO"></span><span id="__irp_buffered_io"></span><dt>

 **\_e/s em buffer de IRP \_**
</dt><span id="IRP_DEALLOCATE_BUFFER"></span><span id="irp_deallocate_buffer"></span><dt>

**\_buffer de DESalocação de IRP \_**
</dt><span id="__IRP_INPUT_OPERATION"></span><span id="__irp_input_operation"></span><dt>

 **\_operação de entrada de IRP \_**
</dt><span id="__IRP_SYNCHRONOUS_PAGING_IO"></span><span id="__irp_synchronous_paging_io"></span><dt>

 **\_ \_ e/s de paginação síncrona IRP \_**
</dt><span id="__IRP_CREATE_OPERATION"></span><span id="__irp_create_operation"></span><dt>

 **\_operação de criação de IRP \_**
</dt><span id="IRP_READ_OPERATION"></span><span id="irp_read_operation"></span><dt>

**\_operação de leitura de IRP \_**
</dt><span id="__IRP_WRITE_OPERATION"></span><span id="__irp_write_operation"></span><dt>

 **\_operação de gravação de IRP \_**
</dt><span id="__IRP_CLOSE_OPERATION"></span><span id="__irp_close_operation"></span><dt>

 **\_operação de fechamento de IRP \_**
</dt><span id="__IRP_DEFER_IO_COMPLETION"></span><span id="__irp_defer_io_completion"></span><dt>

 **\_conclusão de \_ e/s de adiamento de IRP \_**
</dt> </dl>

</dd> <dt>

**IssuingThreadId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (9)
</dt> </dl>

O identificador do thread emissor.

**Windows server 2008 R2, Windows server 2008, Windows 7, Windows Vista, Windows server 2003 com SP1, Windows server 2003, Windows 2000 server e Windows 2000 Professional:** Não há suporte para essa propriedade.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)
</dt> </dl>

Reservado.

**Windows server 2008 R2, Windows server 2008 e Windows 7:** O nome da propriedade é **QueueDepth**, que contém a contagem de tiques da CPU desde o início da operação até o fim da operação. Observe que esse valor pode ser estourado.

**Windows Vista, Windows server 2003 com SP1, Windows server 2003, Windows 2000 server e Windows 2000 Professional:** O nome da propriedade é **ResponseTime**, que contém a contagem de tiques da CPU desde o início da operação até o fim da operação. Observe que esse valor pode ser estourado.

</dd> <dt>

**Transferências**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)
</dt> </dl>

Tamanho dos dados lidos ou gravados do disco, em bytes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Windows O servidor 2003 usa a seguinte definição para a classe de tipo de evento **DiskIo \_ TypeGroup1** .

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

A propriedade **ResponseTime** contém a contagem de tiques da CPU desde o início da operação até o fim da operação. Observe que esse valor pode ser estourado.

Não há suporte para a propriedade **HighResResponseTime** .

Windows o servidor 2003 com SP1 e Windows Vista usa a seguinte definição para a classe de tipo de evento **DiskIo \_ TypeGroup1** .

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

A propriedade **IRP** é o pacote de solicitação de e/s. Essa propriedade identifica a atividade de e/s. Você pode usar essa propriedade com os eventos [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) para correlacionar o tempo de resposta.

Há suporte para a propriedade **HighResResponseTime** . A propriedade contém o tempo entre o início e a conclusão de e/s, conforme medido por PartitionManager (nas unidades KeQueryPerformanceCounter). Use essa propriedade em vez da propriedade **ResponseTime** para determinar o tempo de resposta de e/s do disco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 
