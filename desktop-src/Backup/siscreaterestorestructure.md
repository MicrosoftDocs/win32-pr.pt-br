---
title: Função SisCreateRestoreStructure (Sisbkup. h)
description: Cria uma estrutura de restauração do SIS com base nas informações fornecidas.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Backup de função SisCreateRestoreStructure
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824275"
---
# <a name="siscreaterestorestructure-function"></a>Função SisCreateRestoreStructure

A função **SisCreateRestoreStructure** cria uma estrutura de restauração do SIS com base nas informações fornecidas.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*volumeRoot* \[ no\]
</dt> <dd>

Nome do arquivo da raiz do volume, sem a barra invertida à direita, do volume cujo backup será feito. Por exemplo, especifique "C:" e não "C: \\ ". O volume não pode ser o volume do sistema ou de inicialização.

</dd> <dt>

*sisRestoreStructure* \[ fora\]
</dt> <dd>

Foi retornada a estrutura de restauração do SIS. Essa estrutura deve ser tratada como opaca pelo chamador.

</dd> <dt>

*commonStoreRootPathname* \[ fora\]
</dt> <dd>

Nome do caminho totalmente qualificado do repositório comum do volume especificado. Por exemplo, "c: \\ SIS Common Store".

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ fora\]
</dt> <dd>

Número de arquivos listados no parâmetro *commonStoreFilesToRestore* .

</dd> <dt>

*commonStoreFilesToRestore* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de nomes de arquivo que especifica a lista de arquivos internos usados pelo SIS para gerenciar o volume especificado. Esses arquivos devem ser restaurados ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comuns solicitados pelo [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se for concluída com êxito e **false** caso contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.

## <a name="remarks"></a>Comentários

Essa função estabelece o ambiente de restauração no volume especificado no modo como o [**SisCreateBackupStructure**](siscreatebackupstructure.md) estabelece o ambiente de backup no volume especificado.

Observe que essa função não identificará necessariamente o arquivo de repositório comum ou os arquivos correspondentes a um conjunto de links do SIS na mídia de backup se esses arquivos ou arquivo de armazenamento comuns ainda existirem no disco. O conteúdo de um fluxo de dados do arquivo de armazenamento comum nunca muda depois de ser criado, portanto, se o arquivo já existir no disco, não será necessário restaurá-lo.

Os nomes de arquivos de repositório comuns são globalmente exclusivos para garantir a integridade da operação de restauração, mesmo que não ocorra no mesmo volume habilitado para SIS que a operação de backup tenha acessado.

Depois que a operação de restauração for concluída, Desaloque a memória usada pela matriz *commonStoreFilesToRestore* de cadeias de caracteres chamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> <dt>

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisFreeBackupStructure**](sisfreebackupstructure.md)
</dt> </dl>

 

