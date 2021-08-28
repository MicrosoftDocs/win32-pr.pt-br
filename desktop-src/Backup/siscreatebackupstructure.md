---
title: Função SisCreateBackupStructure (Sisbkup.h)
description: Cria uma estrutura de backup do SIS com base nas informações fornecidas.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Backup da função SisCreateBackupStructure
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655dfe09285e72b0b961f81c26d6afcc4aae53101a3b12b1bf0a9f1823a45d2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021364"
---
# <a name="siscreatebackupstructure-function"></a>Função SisCreateBackupStructure

A **função SisCreateBackupStructure** cria uma estrutura de backup do SIS com base nas informações fornecidas.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*volumeRoot* \[ Em\]
</dt> <dd>

Nome do arquivo da raiz do volume, sem a faixa invertida à frente, do volume a ser feito backup. Por exemplo, especifique "C:" e não "C: \\ ".

</dd> <dt>

*sisBackupStructure* \[ out\]
</dt> <dd>

Estrutura de backup do SIS retornada.

</dd> <dt>

*commonStoreRootPathname* \[ out\]
</dt> <dd>

Nome de caminho totalmente qualificado do armazenamento comum do volume especificado. Por exemplo, "c: \\ Armazenamento Comum do SIS".

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Número de arquivos listados no *parâmetro commonStoreFilesToBackUp.*

</dd> <dt>

*commonStoreFilesToBackUp* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de nomes de arquivo que especifica uma lista de arquivos internos usados pelo SIS para gerenciar o volume especificado. Esses arquivos devem ser armazenados em backup ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comum solicitados por [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retornará **TRUE** se for concluída com êxito e **FALSE caso** contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha da chamada.

## <a name="remarks"></a>Comentários

Essa função cria uma estrutura de backup do SIS, que é usada pela API de backup do SIS para criar e manter uma lista dos links de arquivo no volume e os arquivos originais para os quais os links apontam. Essa função deve ser chamada apenas uma vez para cada volume habilitado para SIS que está sendo feito backup. Todos os arquivos dentro do volume especificado devem ser tratados como arquivos de armazenamento comum e fazer backup somente se o SIS indicar que devem.

Os *parâmetros countOfCommonStoreFilesToBackUp* e *commonStoreFilesToBackUp* retornam uma lista de arquivos que devem ser armazenados em backup, independentemente de quais links são armazenados em backup.

Se *countOfCommonStoreFilesToBackUp* for 0, *commonStoreFilesToBackUp* poderá ser um **ponteiro NULL.** O valor do *parâmetro commonStoreFilesToBackUp* deve ser ignorado.

Após a conclusão da operação de backup, desaloque a memória usada pela matriz *commonStoreFilesToBackUp* de cadeias de caracteres chamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> </dl>

 

