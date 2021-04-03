---
description: Lista arquivos protegidos.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Função SfcGetFiles (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828818"
---
# <a name="sfcgetfiles-function"></a>Função SfcGetFiles

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. O suporte para essa função foi removido no Windows Vista e no Windows Server 2008. Use as funções com suporte listadas em [funções WRP](wfp-functions.md) em vez disso.\]

Lista arquivos protegidos.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtFileData* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ entrada de arquivo PPROTECT**](pprotect-file-entry.md) que contém a lista de arquivos protegidos.

</dd> <dt>

*Contagem de FileCount* \[ fora\]
</dt> <dd>

Um ponteiro para um local que contém um valor ULONG que é o número de arquivos protegidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no status. Se a função falhar, ela retornará o código de erro NTSTATUS apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_entrada de arquivo PPROTECT \_**](pprotect-file-entry.md)
</dt> </dl>

 

 




