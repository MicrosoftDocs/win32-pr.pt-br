---
description: Contém informações sobre o tamanho de um dispositivo. Isso é retornado do código de \_ controle de capacidade de leitura do armazenamento do IOCTL \_ \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: Estrutura de STORAGE_READ_CAPACITY (Ntddstor. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370386"
---
# <a name="storage_read_capacity-structure"></a>Estrutura de capacidade de \_ leitura de armazenamento \_

Contém informações sobre o tamanho de um dispositivo. Isso é retornado do código de controle de [**capacidade de leitura do armazenamento do IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a>Membros

<dl> <dt>

**Versão**
</dt> <dd>

A versão desta estrutura. O chamador deve definir esse membro como `sizeof(STORAGE_READ_CAPACITY)` .

</dd> <dt>

**Tamanho**
</dt> <dd>

O tamanho dos dados retornados.

</dd> <dt>

**BlockLength**
</dt> <dd>

O número de bytes por bloco.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd>

O número total de blocos no disco.

</dd> <dt>

**DiskLength**
</dt> <dd>

O tamanho do disco em bytes.

</dd> </dl>

## <a name="remarks"></a>Comentários

O arquivo de cabeçalho Ntddstor. h está disponível no WDK (Kit de driver do Windows).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2003 com SP1<br/>                          |
| parâmetro<br/>                   | <dl> <dt>Ntddstor. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_capacidade de \_ leitura do armazenamento do IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




