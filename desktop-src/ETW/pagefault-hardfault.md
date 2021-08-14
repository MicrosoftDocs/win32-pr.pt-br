---
description: Essa classe é a classe de tipo de evento para eventos de falha de página de hardware. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 9837cc45-6485-46c3-a5d9-0d33e443cd32
title: Classe PageFault_HardFault
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_HardFault
- PageFault_HardFault.InitialTime
- PageFault_HardFault.ReadOffset
- PageFault_HardFault.VirtualAddress
- PageFault_HardFault.FileObject
- PageFault_HardFault.TThreadId
- PageFault_HardFault.ByteCount
api_type:
- NA
api_location: ''
ms.openlocfilehash: fdabfab80eadc75fa05ffe148363a85cb5ddefad9abb626cfa4e1c3fa6fe2a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394609"
---
# <a name="pagefault_hardfault-class"></a>\_Classe falhadepágina HardFault

Essa classe é a classe de tipo de evento para eventos de falha de página de hardware.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType{32}, EventTypeName{"HardFault"}]
class PageFault_HardFault : PageFault_V2
{
  object InitialTime;
  uint64 ReadOffset;
  uint32 VirtualAddress;
  uint32 FileObject;
  uint32 TThreadId;
  uint32 ByteCount;
};
```

## <a name="members"></a>Membros

A classe **falhadepágina \_ HardFault** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **falhadepágina \_ HardFault** tem essas propriedades.

<dl> <dt>

**ByteCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (6)
</dt> </dl>

Quantidade de dados lidos de ReadOffset para satisfazer a falha.

</dd> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (4), ponteiro
</dt> </dl>

Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**de \_ nome de FileIo**](fileio-name.md) para determinar o nome do arquivo.

</dd> <dt>

**Inicialtime**
</dt> <dd> <dl> <dt>

Tipo de dados: **objeto**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), extensão ("WmiTime")
</dt> </dl>

Carimbo de data/hora de início em que a falha de página ocorreu.

</dd> <dt>

**ReadOffset**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (2), formato ("x")
</dt> </dl>

Deslocamento de arquivo do qual os dados foram lidos para atender à falha.

</dd> <dt>

**TThreadId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (5), formato ("x")
</dt> </dl>

Identificador de thread do thread que encontrou a falha de página.

</dd> <dt>

**VirtualAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (3), ponteiro
</dt> </dl>

Endereço com falha.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Falhadepágina \_ v2**](pagefault-v2.md)
</dt> </dl>

 

 




