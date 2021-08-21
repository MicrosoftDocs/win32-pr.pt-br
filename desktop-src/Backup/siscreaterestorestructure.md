---
title: Função SisCreateRestoreStructure (Sisbkup.h)
description: Cria uma estrutura de restauração do SIS com base nas informações fornecidas.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Backup da função SisCreateRestoreStructure
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
ms.openlocfilehash: 7e2d8ae0033659392c43fc833c66a4ed9d9b7f75790bda2822f0bd6b5db7f0cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173987"
---
# <a name="siscreaterestorestructure-function"></a>Função SisCreateRestoreStructure

A **função SisCreateRestoreStructure** cria uma estrutura de restauração do SIS com base nas informações fornecidas.

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

*volumeRoot* \[ Em\]
</dt> <dd>

Nome do arquivo da raiz do volume, sem a faixa invertida à frente, do volume a ser feito backup. Por exemplo, especifique "C:" e não "C: \\ ". O volume não pode ser o sistema ou o volume de inicialização.

</dd> <dt>

*sisRestoreStructure* \[ out\]
</dt> <dd>

Estrutura de restauração do SIS retornada. Essa estrutura deve ser tratada como opaca pelo chamador.

</dd> <dt>

*commonStoreRootPathname* \[ out\]
</dt> <dd>

Nome de caminho totalmente qualificado do armazenamento comum do volume especificado. Por exemplo, "c: \\ Armazenamento Comum do SIS".

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ out\]
</dt> <dd>

Número de arquivos listados no *parâmetro commonStoreFilesToRestore.*

</dd> <dt>

*commonStoreFilesToRestore* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de nomes de arquivo que especifica a lista de arquivos internos usados pelo SIS para gerenciar o volume especificado. Esses arquivos devem ser restaurados ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comum solicitados por [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retornará **TRUE** se for concluída com êxito e **FALSE caso** contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha da chamada.

## <a name="remarks"></a>Comentários

Essa função estabelece o ambiente de restauração no volume especificado da maneira como [**SisCreateBackupStructure**](siscreatebackupstructure.md) estabelece o ambiente de backup no volume especificado.

Observe que essa função não identificará necessariamente o arquivo ou arquivos de armazenamento comum correspondentes a um conjunto de links do SIS na mídia de backup se esses arquivos ou arquivos comuns do armazenamento ainda existirem no disco. O conteúdo do fluxo de dados de um arquivo de armazenamento comum nunca muda depois que ele é criado, portanto, se o arquivo já existir no disco, não será necessário restaurá-lo.

Os nomes de arquivo de armazenamento comum são globalmente exclusivos para garantir a integridade da operação de restauração, mesmo que ela não ocorra no mesmo volume habilitado para SIS acessado pela operação de backup.

Depois que a operação de restauração for concluída, desaloque a memória usada pela matriz *commonStoreFilesToRestore* de cadeias de caracteres chamando [**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md).

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

[**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisFreeBackupStructure**](sisfreebackupstructure.md)
</dt> </dl>

 

