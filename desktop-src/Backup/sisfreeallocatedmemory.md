---
title: Função SisFreeAllocatedMemory (Sisbkup.h)
description: Libera a memória alocada pelas funções de API do SIS.
ms.assetid: 8fab79c8-593c-46df-a885-09a59620a977
keywords:
- Backup da função SisFreeAllocatedMemory
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
ms.openlocfilehash: a4510e464c2201952823d144721614caa7b5f1397c68f4f129dac73a4015b86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702176"
---
# <a name="sisfreeallocatedmemory-function"></a>Função SisFreeAllocatedMemory

A **função SisFreeAllocatedMemory** libera a memória alocada pelas funções de API do SIS.

## <a name="syntax"></a>Sintaxe


```C++
void SisFreeAllocatedMemory(
  _In_ PVOID allocatedSpace
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*allocatedSpace* \[ Em\]
</dt> <dd>

Ponteiro para a memória alocada pela API do SIS.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Depois que a chamada para essa função for concluída, o chamador poderá não acessar mais a memória liberada.

Essa chamada deve ser usada para desalocar a memória alocada para as cadeias de caracteres de parâmetro *commonStoreRootPathname* retornadas de [**SisCreateBackupStructure**](siscreatebackupstructure.md) e [**SisCreateRestoreStructure**](siscreaterestorestructure.md)e a matriz de cadeias de caracteres que contêm nomes de arquivo de repositório comum retornados de **SisCreateBackupStructure**, [**SisCSFilesToBackupForLink,**](siscsfilestobackupforlink.md) **SisCreateRestoreStructure** e [**SisRestoredLink**](sisrestoredlink.md). No último caso, a matriz em si também deve ser liberada chamando **SisFreeAllocatedMemory**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
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

 

 





