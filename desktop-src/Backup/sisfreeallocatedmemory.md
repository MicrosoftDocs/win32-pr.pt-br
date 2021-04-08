---
title: Função SisFreeAllocatedMemory (Sisbkup. h)
description: Libera memória alocada pelas funções de API do SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Backup de função SisFreeAllocatedMemory
topic_type:
- apiref
api_name:
- SisFreeAllocatedMemory
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724970817b89f6a9f2490b0776775f6a3a4e69ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824274"
---
# <a name="sisfreeallocatedmemory-function"></a>Função SisFreeAllocatedMemory

A função **SisFreeAllocatedMemory** libera a memória alocada pelas funções de API do SIS.

## <a name="syntax"></a>Sintaxe


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*allocatedSpace* \[ no\]
</dt> <dd>

Ponteiro para a memória alocada pela API do SIS.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Depois que a chamada para essa função for concluída, o chamador poderá não acessar mais a memória liberada.

Essa chamada deve ser usada para desalocar a memória alocada para as cadeias de caracteres de parâmetro *commonStoreRootPathname* retornadas de [**SisCreateBackupStructure**](siscreatebackupstructure.md) e [**SisCreateRestoreStructure**](siscreaterestorestructure.md), e a matriz de cadeias de caracteres que contém nomes de arquivo de repositório comum retornado de **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md), **SisCreateRestoreStructure** e [**SisRestoredLink**](sisrestoredlink.md). No último caso, a própria matriz também deve ser liberada chamando **SisFreeAllocatedMemory**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

 





