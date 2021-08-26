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
ms.openlocfilehash: 3201621808708229419542acd7fa0caab0aa7f6e7d38bfe723b7f53bc68c4005
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999276"
---
# <a name="sfcgetfiles-function"></a>Função SfcGetFiles

\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos. o suporte para essa função foi removido no Windows Vista e no Windows Server 2008. Use as funções com suporte listadas em [funções WRP](wfp-functions.md) em vez disso.\]

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

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será \_ êxito no status. Se a função falhar, ela retornará o código de erro NTSTATUS apropriado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                                                   |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Sfcfiles. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Sfcfiles.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_entrada de arquivo PPROTECT \_**](pprotect-file-entry.md)
</dt> </dl>

 

 




