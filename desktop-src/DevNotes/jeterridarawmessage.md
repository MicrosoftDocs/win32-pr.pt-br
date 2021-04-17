---
description: Recupera uma cadeia de caracteres de mensagem não formatada quando um identificador de código de erro (IDA) é fornecido.
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: Função JetErrIDARawMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749412"
---
# <a name="jeterridarawmessage-function"></a>Função JetErrIDARawMessage

Recupera uma cadeia de caracteres de mensagem não formatada quando um identificador de código de erro (IDA) é fornecido.

## <a name="syntax"></a>Sintaxe


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ida* 
</dt> <dd>

Um número que mapeia para um código de erro específico e é exibido para o usuário.

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

## <a name="return-value"></a>Retornar valor

Se a função tiver êxito, ela retornará **Jet \_ errSuccess**; caso contrário, ela retornará uma mensagem não formatada que indica o motivo específico da falha.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
