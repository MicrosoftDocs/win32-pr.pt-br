---
title: Função SisCreateBackupStructure (Sisbkup. h)
description: Cria uma estrutura de backup do SIS com base nas informações fornecidas.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Backup de função SisCreateBackupStructure
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
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454883"
---
# <a name="siscreatebackupstructure-function"></a>Função SisCreateBackupStructure

A função **SisCreateBackupStructure** cria uma estrutura de backup do SIS com base nas informações fornecidas.

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

*volumeRoot* \[ no\]
</dt> <dd>

Nome do arquivo da raiz do volume, sem a barra invertida à direita, do volume cujo backup será feito. Por exemplo, especifique "C:" e não "C: \\ ".

</dd> <dt>

*sisBackupStructure* \[ fora\]
</dt> <dd>

A estrutura de backup do SIS foi retornada.

</dd> <dt>

*commonStoreRootPathname* \[ fora\]
</dt> <dd>

Nome do caminho totalmente qualificado do repositório comum do volume especificado. Por exemplo, "c: \\ SIS Common Store".

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ fora\]
</dt> <dd>

Número de arquivos listados no parâmetro *commonStoreFilesToBackUp* .

</dd> <dt>

*commonStoreFilesToBackUp* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de nomes de arquivo que especifica uma lista de arquivos internos usados pelo SIS para gerenciar o volume especificado. Esses arquivos devem ser armazenados em backup ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comuns solicitados pelo [ **SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se for concluída com êxito e **false** caso contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.

## <a name="remarks"></a>Comentários

Essa função cria uma estrutura de backup do SIS, que é usada pela API de backup do SIS para criar e manter uma lista de links de arquivos no volume e nos arquivos originais aos quais os links apontam. Essa função deve ser chamada apenas uma vez para cada volume habilitado para SIS que está sendo submetido a backup. Todos os arquivos no volume especificado devem ser tratados como arquivos de armazenamento comum e armazenados em backup somente se o SIS indicar que deveria.

Os parâmetros *countOfCommonStoreFilesToBackUp* e *commonStoreFilesToBackUp* juntos retornam uma lista de arquivos que devem ser copiados em backup, independentemente de quais links são incluídos no backup.

Se *countOfCommonStoreFilesToBackUp* for 0, *commonStoreFilesToBackUp* poderá ser um ponteiro **nulo** . O valor do parâmetro *commonStoreFilesToBackUp* deve ser ignorado.

Depois que a operação de backup for concluída, Desaloque a memória usada pela matriz *commonStoreFilesToBackUp* de cadeias de caracteres chamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> </dl>

 

