---
description: Recupera uma cadeia de caracteres de mensagem não formatada quando um IDA (identificador de código de erro) é fornecido.
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
ms.openlocfilehash: 39bd07b3ac75bed85ff26dd7f014420ebaca8be16d6f0195d40e9161c0905496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955755"
---
# <a name="jeterridarawmessage-function"></a>Função JetErrIDARawMessage

Recupera uma cadeia de caracteres de mensagem não formatada quando um IDA (identificador de código de erro) é fornecido.

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

*pwszHelp/file* 
</dt> <dd>

Um ponteiro para um ponteiro para o arquivo que explica o erro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará **JET \_ errSuccess;** caso contrário, ela retornará uma mensagem não formatada que indica o motivo específico da falha.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
