---
description: Conclui a configuração de um buffer de rastreamento com campos opcionais para rastreamentos de estilo sprintf.
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
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751355"
---
# <a name="asyncstringtrace-function"></a>Função AsyncStringTrace

Conclui a configuração de um buffer de rastreamento com campos opcionais para rastreamentos de estilo **sprintf**.

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

Um parâmetro de rastreamento de 32 bits que é usado para filtragem no nível do aplicativo.

</dd> <dt>

*szFormat* 
</dt> <dd>

Uma cadeia de caracteres terminada em zero que descreve o formato do rastreamento.

</dd> <dt>

*Marker* 
</dt> <dd>

Um marcador para as funções **vsprintf** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna o comprimento da instrução Trace, em bytes.

## <a name="remarks"></a>Comentários

Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP (Network News Transfer Protocol).

O tipo de dados da **\_ lista de VA** é um tipo padrão usado para manter as informações necessárias pelas macros **VA \_ ARG** e **VA \_ end** . Para obter mais informações, consulte [tipos padrão](/cpp/c-runtime-library/standard-types?view=vs-2019).

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

