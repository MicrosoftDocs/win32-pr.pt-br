---
description: Recupera um IDA (identificador de código de erro) e cria a cadeia de caracteres de exibição final quando um erro de Jet e informações de erro estendidas são fornecidas.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: Função JetErrFormattedMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8b0fa6eb0ac4bc29e5657d3e58d9be1c27188a0faf7c7d68281ceca239dea8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955775"
---
# <a name="jeterrformattedmessage-function"></a>Função JetErrFormattedMessage

Recupera um IDA (identificador de código de erro) e cria a cadeia de caracteres de exibição final quando um erro de Jet e informações de erro estendidas são fornecidas.

## <a name="syntax"></a>Sintaxe


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*erra* 
</dt> <dd>

O número do erro Jet que é usado para pesquisar e formatar a mensagem de erro exibível.

</dd> <dt>

*pExtendedErrorInfo* 
</dt> <dd>

Todas as informações de erro do Jet, incluindo o nome do banco de dados, o nome da tabela e qualquer informação de erro secundária.

</dd> <dt>

*pIda* 
</dt> <dd>

Um ponteiro para o IDA que está associado ao código de erro específico.

</dd> <dt>

*pMessage* 
</dt> <dd>

Um ponteiro para a mensagem de erro.

</dd> <dt>

*cbMessage* 
</dt> <dd>

Uma contagem do número de bytes na mensagem de erro.

</dd> <dt>

*pcbActual* 
</dt> <dd>

Um ponteiro para o número real de bytes lidos.

</dd> <dt>

*pContextId* 
</dt> <dd>

Um ponteiro para o identificador de contexto associado ao arquivo de ajuda.

</dd> <dt>

*pwszHelp/arquivo* 
</dt> <dd>

Um ponteiro para um ponteiro para o arquivo que explica o erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com êxito, ela retornará **Jet \_ errSuccess**; caso contrário, ela retornará uma mensagem de erro formatada que indica o motivo específico da falha.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
