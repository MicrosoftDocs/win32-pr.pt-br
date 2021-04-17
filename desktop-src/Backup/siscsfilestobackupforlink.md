---
title: Função SisCSFilesToBackupForLink (Sisbkup. h)
description: Retorna informações que descrevem os arquivos de armazenamento comuns aos quais o link do SIS especificado aponta.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Backup de função SisCSFilesToBackupForLink
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755462"
---
# <a name="siscsfilestobackupforlink-function"></a>Função SisCSFilesToBackupForLink

A função **SisCSFilesToBackupForLink** retorna informações que descrevem os arquivos de armazenamento comuns aos quais o link do SIS especificado aponta.

## <a name="syntax"></a>Sintaxe


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sisBackupStructure* \[ no\]
</dt> <dd>

Ponteiro para a estrutura de backup do SIS retornada de [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> <dt>

*reparseData* \[ no\]
</dt> <dd>

Ponteiro para o conteúdo do ponto de nova análise do SIS. Esse ponto de nova análise contém dados que descrevem um link do SIS. Para recuperar os dados do ponto de nova análise de um arquivo, use o código de controle [**fsctl \_ Get de \_ \_ ponto de nova análise**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) .

</dd> <dt>

*reparseDataSize* \[ no\]
</dt> <dd>

Tamanho do conteúdo do ponto de nova análise do SIS apontado por *reparseData*, em bytes.

</dd> <dt>

*thisFileContext* \[ fora\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres de contexto fornecida pelo aplicativo de backup que chama essa função. O conteúdo dessa cadeia de caracteres de conteúdo é totalmente determinado por esse aplicativo de backup e não é interpretado pela API de backup do SIS. Esse parâmetro é opcional; Se não for usado, defina o valor desse parâmetro como **NULL**. O valor desse parâmetro não será processado nesse caso.

</dd> <dt>

*matchingFileContext* \[ fora\]
</dt> <dd>

Ponteiro de indireto duplo para a cadeia de caracteres de contexto do link do SIS identificado pelas informações passadas nos quatro primeiros parâmetros dessa função. Esse parâmetro é opcional; se uma cadeia de caracteres de contexto não for fornecida como o valor do parâmetro *thisFileContext* , defina o valor desse parâmetro como **NULL**. O valor desse parâmetro não será processado nesse caso.

</dd> <dt>

*countOfCommonStoreFilesToBackUp* \[ fora\]
</dt> <dd>

Número de arquivos listados no parâmetro *commonStoreFilesToBackUp* .

</dd> <dt>

*commonStoreFilesToBackUp* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de nomes de arquivo. Esses arquivos devem ser armazenados em backup ao mesmo tempo e da mesma maneira que os arquivos de armazenamento comuns solicitados pelo [**SisCreateBackupStructure**](siscreatebackupstructure.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará **true** se for concluída com êxito e **false** caso contrário. Chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações sobre o motivo da falha na chamada.

## <a name="remarks"></a>Comentários

O aplicativo de backup deve chamar essa função apenas uma vez para cada arquivo de link do SIS cujo backup está sendo feito.

O aplicativo de backup pode identificar um ponto de nova análise do SIS por sua marca, a marca de nova análise de e/s \_ \_ \_ SIS. Essa marca é definida em Winnt. h.

Se esse ponto de nova análise identificado pelo valor do parâmetro *reparseData* descrever a primeira instância de um arquivo a ser armazenado em backup, essa função retornará **NULL** como o valor do parâmetro *matchingFileContext* e inicializará o valor da matriz *commonStoreFilesToBackUp* de cadeias de caracteres com os nomes do arquivo de armazenamento comum ou dos arquivos cujo backup será feito. Caso contrário, essa função definirá o valor do parâmetro *matchingFileContext* como a cadeia de caracteres de contexto correspondente à primeira instância do arquivo especificado e definirá o valor do parâmetro *countOfCommonStoreFilesToBackUp* como 0. Se houver vários arquivos de repositório comum correspondentes ao link especificado, o valor do parâmetro *thisFileContext* será a cadeia de caracteres de contexto correspondente ao primeiro arquivo de repositório comum retornado na matriz, que é, commonStoreFilesToBackUp \[ 0 \] .

A versão atual dessa função retornará no máximo um arquivo de armazenamento comum, mas é possível que, em versões futuras, um único link possa ser apoiado por vários arquivos de armazenamento comum, por exemplo, um para cada fluxo no arquivo, de modo que o aplicativo de backup deve dar suporte a vários arquivos em cada chamada para essa função. Em qualquer caso, cada arquivo de repositório comum será retornado no máximo uma vez para cada passagem de backup.

O aplicativo de backup deve fazer backup ou restaurar o arquivo de repositório comum ou os arquivos identificados pelo nome do arquivo ou pelos nomes de arquivo retornados no parâmetro *commonStoreFilesToBackUp* . Independentemente de haver um arquivo de repositório comum correspondente, o aplicativo de backup deve fazer backup do arquivo de link do SIS como ele existe no disco, por exemplo, como um ponto de nova análise e um arquivo esparso, e provavelmente sem intervalos preenchidos. Seu aplicativo de backup pode fazer backup ou restaurar o arquivo de armazenamento comum ou os arquivos imediatamente, adiar o backup deles ou combiná-los conforme necessário.

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

[**SisFreeAllocatedMemory**](sisfreeallocatedmemory.md)
</dt> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

