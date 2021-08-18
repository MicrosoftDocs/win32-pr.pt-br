---
description: Recupera um IDA (identificador de código de erro) e uma cadeia de caracteres de mensagem não formatada quando um erro jet é fornecido.
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
ms.openlocfilehash: efc7332530b5b03b0c9150adb8b0e105d0e5d17eeae9bbc485fb073391de2cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749676"
---
# <a name="jeterrrawmessage-function"></a>Função JetErrRawMessage

Recupera um IDA (identificador de código de erro) e uma cadeia de caracteres de mensagem não formatada quando um erro jet é fornecido.

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

*Err* 
</dt> <dd>

O erro jet que corresponde às informações que estão sendo obtidas.

</dd> <dt>

*pIda* 
</dt> <dd>

Um ponteiro para o IDA.

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

*pwszHelp/file* 
</dt> <dd>

Aponta para um ponteiro para o arquivo que explica o erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará **JET \_ errSuccess;** caso contrário, retornará uma mensagem de erro não formatada que indica o motivo específico da falha.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
