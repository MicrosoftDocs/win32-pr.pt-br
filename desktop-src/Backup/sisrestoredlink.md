---
title: Função SisRestoredLink (Sisbkup. h)
description: Retorna os nomes do arquivo de repositório comum ou dos arquivos apontados pelo link SIS restaurado especificado.
ms.assetid: 4eefd975-6055-44c0-93ab-900638948f3e
keywords:
- Backup de função SisRestoredLink
topic_type:
- apiref
api_name:
- SisRestoredLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd539d1ad6c203441b2bcd469a7d8f2fe8bdfc7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918176"
---
# <a name="sisrestoredlink-function"></a>Função SisRestoredLink

A função **SisRestoredLink** retorna os nomes do arquivo de repositório comum ou arquivos apontados pelo link SIS restaurado especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SisRestoredLink(
  _In_  PVOID  sisRestoreStructure,
  _In_  PWCHAR restoredFileName,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sisRestoreStructure* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de restauração do SIS retornada de [**SisCreateRestoreStructure**](siscreaterestorestructure.md).

</dd> <dt>

*restoredFileName* \[ no\]
</dt> <dd>

Nome de arquivo totalmente qualificado do arquivo de link do SIS restaurado.

</dd> <dt>

*reparseData* \[ no\]
</dt> <dd>

Ponteiro para o conteúdo do ponto de nova análise do SIS. Esse ponto de nova análise contém dados que descrevem o link do SIS restaurado. Para recuperar os dados do ponto de nova análise de um arquivo, use o código de controle [**fsctl \_ Get de \_ \_ ponto de nova análise**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .

</dd> <dt>

*reparseDataSize* \[ no\]
</dt> <dd>

Tamanho do conteúdo do ponto de nova análise do SIS apontado por *reparseData*, em bytes.

</dd> <dt>

*countOfCommonStoreFilesToRestore* \[ fora\]
</dt> <dd>

Número de arquivos listados no parâmetro *commonStoreFilesToRestore* .

</dd> <dt>

*commonStoreFilesToRestore* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de nomes de arquivos de repositório comum. Esses arquivos devem ser restaurados ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comuns solicitados pelo [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md).

Se o valor do parâmetro *countOfCommonStoreFilesToRestore* não for 0, o valor do parâmetro *commonStoreFilesToRestore* conterá os nomes dos arquivos de armazenamento comuns a serem restaurados como resultado da restauração do link do SIS. Se o valor for 0, os arquivos de armazenamento comum foram retornados uma vez ou já estão presentes no volume.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se for concluída com êxito e **false** caso contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.

## <a name="remarks"></a>Comentários

Você deve chamar essa função para cada link do SIS que foi restaurado.

Esta função retornará cada arquivo de repositório comum no máximo uma vez para cada operação de restauração; qualquer tentativa de restaurar links adicionais do SIS que veem o mesmo arquivo de armazenamento comum não resultará no retorno do nome do arquivo de repositório comum.

Essa função não retornará um arquivo de repositório comum que também não foi retornado em uma chamada para [**SisCSFilesToBackupForLink**](siscsfilestobackupforlink.md) durante a operação de backup, supondo que os dados de nova análise do SIS armazenados na mídia não tenham sido corrompidos.

Ao restaurar um link do SIS, a operação de restauração deve criar apenas o arquivo esparso apropriado, inicializar os intervalos alocados e, em seguida, gravar os dados de nova análise do SIS exatamente como eles foram lidos durante a operação de backup. É crucial que a operação de restauração Crie arquivos esparsos com intervalos não alocados em vez de arquivos esparsos (ou arquivos não SPARSE) inicializados com zeros.

Observe que essa função não identificará necessariamente o arquivo de repositório comum ou os arquivos correspondentes a um conjunto de links do SIS na mídia de backup se esses arquivos ou arquivo de armazenamento comum ainda existirem no disco. O conteúdo de um fluxo de dados do arquivo de armazenamento comum nunca muda depois de ser criado, portanto, se o arquivo já existir no disco, não será necessário restaurá-lo.

Os nomes de arquivos de repositório comuns são globalmente exclusivos para garantir a integridade da operação de restauração, mesmo que não ocorra no mesmo volume habilitado para SIS que a operação de backup tenha acessado.

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
</dt> </dl>

 

