---
title: Função SisRestoredCommonStoreFile (Sisbkup. h)
description: Relata para a arquitetura do SIS que um arquivo de armazenamento comum foi gravado.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Backup de função SisRestoredCommonStoreFile
topic_type:
- apiref
api_name:
- SisRestoredCommonStoreFile
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 093ff5f20db42bcafe62ee0ec57d5027abcf9f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918177"
---
# <a name="sisrestoredcommonstorefile-function"></a>Função SisRestoredCommonStoreFile

A função **SisRestoredCommonStoreFile** relata para a arquitetura do SIS que um arquivo de armazenamento comum foi gravado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sisRestoreStructure* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de restauração do SIS retornada de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*commonStoreFileName* \[ no\]
</dt> <dd>

Nome do arquivo de repositório comum restaurado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se for concluída com êxito e **false** caso contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.

## <a name="remarks"></a>Comentários

Essa função deve ser chamada depois que você tiver restaurado um arquivo de repositório comum. Ele notifica a arquitetura do SIS que um novo arquivo de armazenamento comum foi gravado, para que a arquitetura do SIS possa executar tarefas de manutenção internas, como inicializar suas estruturas de dados internas ou corrigir os links para o arquivo de repositório comum.

A operação de restauração deve restaurar somente os arquivos de repositório comuns relatados pelo [**SisRestoredLink**](sisrestoredlink.md), mesmo se houver arquivos de repositório comum adicionais na mídia de backup. A operação de restauração pode restaurar os links do SIS e os arquivos de armazenamento comum em qualquer ordem escolhida; no entanto, ele deve chamar **SisRestoredLink** depois de restaurar qualquer link e deve chamar essa função depois de restaurar qualquer arquivo de repositório comum. Como a operação de restauração não pode identificar quais arquivos de armazenamento comum serão restaurados até que os nomes de arquivo sejam relatados a ele como resultado da restauração de um link, a operação de restauração sempre restaurará um arquivo de repositório comum depois que pelo menos um link fizer referência a ele for restaurado. No entanto, você pode restaurar outros links do SIS que apontam para o arquivo de armazenamento comum.

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

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

