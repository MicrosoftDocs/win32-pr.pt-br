---
description: Contém informações sobre o tamanho de um dispositivo. Isso é retornado do código de controle IOCTL \_ STORAGE \_ READ \_ CAPACITY.
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: STORAGE_READ_CAPACITY (Ntddstor.h)
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
ms.openlocfilehash: 3a138f6594e241c96526ebf6955c61374aa0f48a5aa66f364ef82c1591b64594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404967"
---
# <a name="storage_read_capacity-structure"></a>Estrutura STORAGE \_ READ \_ CAPACITY

Contém informações sobre o tamanho de um dispositivo. Isso é retornado do código [**de controle IOCTL \_ STORAGE READ \_ \_ CAPACITY.**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)

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

A versão dessa estrutura. O chamador deve definir esse membro como `sizeof(STORAGE_READ_CAPACITY)` .

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

O arquivo de título Ntddstor.h está disponível no WDK (Kit Windows Driver).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2008, Windows Server 2003 com SP1<br/>                          |
| parâmetro<br/>                   | <dl> <dt>Ntddstor.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CAPACIDADE DE LEITURA DO ARMAZENAMENTO IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




