---
description: Recupera um IDA (identificador de código de erro) e uma cadeia de caracteres de mensagem não formatada quando um erro de Jet é fornecido.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: Função JetErrRawMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751955"
---
# <a name="jeterrrawmessage-function"></a>Função JetErrRawMessage

Recupera um IDA (identificador de código de erro) e uma cadeia de caracteres de mensagem não formatada quando um erro de Jet é fornecido.

## <a name="syntax"></a>Sintaxe


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
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

O erro de Jet que corresponde às informações que estão sendo obtidas.

</dd> <dt>

*pIda* 
</dt> <dd>

Um ponteiro para IDA.

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

Aponta para um ponteiro para o arquivo que explica o erro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com êxito, ela retornará **Jet \_ errSuccess**; caso contrário, ela retornará uma mensagem de erro não formatada que indica o motivo específico da falha.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
