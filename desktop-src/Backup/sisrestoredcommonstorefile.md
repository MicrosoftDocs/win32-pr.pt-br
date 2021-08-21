---
title: Função SisRestoredCommonStoreFile (Sisbkup.h)
description: Relata à arquitetura do SIS que um arquivo de armazenamento comum foi gravado.
ms.assetid: 2b1cd9e7-a19c-4474-a40a-5a27d4feeab7
keywords:
- Backup da função SisRestoredCommonStoreFile
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
ms.openlocfilehash: 389d40b76614fe64038133c8cc0623706d4f2be82e68b3e096b59b3023f08bf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529486"
---
# <a name="sisrestoredcommonstorefile-function"></a>Função SisRestoredCommonStoreFile

A **função SisRestoredCommonStoreFile** relata à arquitetura do SIS que um arquivo de repositório comum foi gravado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SisRestoredCommonStoreFile(
  _In_ PVOID  sisRestoreStructure,
  _In_ PWCHAR commonStoreFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sisRestoreStructure* \[ Em\]
</dt> <dd>

Ponteiro para uma estrutura de restauração do SIS retornada de [**SisCreateRestoreStructure.**](siscreaterestorestructure.md)

</dd> <dt>

*commonStoreFileName* \[ Em\]
</dt> <dd>

Nome do arquivo de armazenamento comum restaurado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retornará **TRUE** se for concluída com êxito e **FALSE caso** contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha da chamada.

## <a name="remarks"></a>Comentários

Essa função deve ser chamada depois que você tiver restaurado um arquivo de armazenamento comum. Ele notifica a arquitetura do SIS de que um novo arquivo de armazenamento comum foi gravado, para que a arquitetura do SIS possa executar tarefas de manutenção internas, como inicializar suas estruturas de dados internas ou corrigir os links para o arquivo de armazenamento comum.

Sua operação de restauração deve restaurar somente arquivos de armazenamento comum relatados por [**SisRestoredLink**](sisrestoredlink.md), mesmo se houver arquivos de armazenamento comum adicionais na mídia de backup. Sua operação de restauração pode restaurar os links do SIS e arquivos de armazenamento comum em qualquer ordem escolhida; No entanto, ele deve chamar **SisRestoredLink** depois de restaurar qualquer link e deve chamar essa função depois de restaurar qualquer arquivo de armazenamento comum. Como a operação de restauração não pode identificar quais arquivos de armazenamento comum serão restaurados até que os nomes de arquivo sejam relatados a ele como resultado da restauração de um link, sua operação de restauração sempre restaurará um arquivo de armazenamento comum depois que pelo menos um link que se refere a ele for restaurado. No entanto, você pode restaurar links adicionais do SIS que apontam para esse arquivo de armazenamento comum.

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

[**SisRestoredLink**](sisrestoredlink.md)
</dt> </dl>

 

