---
description: Função AsyncStringTrace – termina a configuração de um buffer de rastreamento com campos opcionais para rastreamentos no estilo sprintf.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Função AsyncStringTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: ac099b0b69c1417c428aefe04b8e6591f945545a2b69196da588ebce8de23f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076170"
---
# <a name="asyncstringtrace-function"></a>Função AsyncStringTrace

Termina a configuração de um buffer de rastreamento com campos opcionais para **rastreamentos de estilo sprintf.**

## <a name="syntax"></a>Sintaxe


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um parâmetro de rastreamento de 32 bits usado para filtragem no nível do aplicativo.

</dd> <dt>

*szFormat* 
</dt> <dd>

Uma cadeia de caracteres terminada em zero que descreve o formato do rastreamento.

</dd> <dt>

*Marcador* 
</dt> <dd>

Um marcador para **funções vsprintf.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retorna o comprimento da instrução de rastreamento, em bytes.

## <a name="remarks"></a>Comentários

Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP.

O **tipo de dados va \_ list** é um tipo padrão usado para manter as informações necessárias para as macros **va \_ arg** **e va \_ end.** Para obter mais informações, consulte [Tipos padrão](/cpp/c-runtime-library/standard-types?view=vs-2019).

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

