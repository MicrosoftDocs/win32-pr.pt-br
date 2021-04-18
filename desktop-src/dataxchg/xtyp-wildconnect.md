---
title: Transação de XTYP_WILDCONNECT (ddeml. h)
description: Permite que um cliente estabeleça uma conversa em cada nome de serviço do servidor e pares de nome de tópico que correspondam ao nome do serviço especificado e ao nome do tópico.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- Troca de dados de transação XTYP_WILDCONNECT
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762983"
---
# <a name="xtyp_wildconnect-transaction"></a>\_Transação XTYP WILDCONNECT

Permite que um cliente estabeleça uma conversa em cada nome de serviço do servidor e pares de nome de tópico que correspondam ao nome do serviço especificado e ao nome do tópico. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica um nome de serviço **nulo** , um nome de tópico **nulo** ou ambos em uma chamada para a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) ou [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uType* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

Não usado.

</dd> <dt>

*hconv* 
</dt> <dd>

Não usado.

</dd> <dt>

*hsz1* 
</dt> <dd>

Um identificador para o nome do tópico. Se esse parâmetro for **nulo**, o cliente está solicitando uma conversa em todos os nomes de tópico aos quais o servidor dá suporte.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um identificador para o nome do serviço. Se esse parâmetro for **nulo**, o cliente está solicitando uma conversa em todos os nomes de serviço aos quais o servidor dá suporte.

</dd> <dt>

*hdata* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData1* 
</dt> <dd>

Um ponteiro para uma estrutura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contém informações de contexto para a conversa. Se o cliente não for um aplicativo DDEML, esse parâmetro será definido como 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica se o cliente é a mesma instância de aplicativo que o servidor. Se o parâmetro for 1, o cliente será a mesma instância. Se o parâmetro for 0, o cliente será uma instância diferente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O servidor deve retornar um identificador de dados que identifica uma matriz de estruturas [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) . A matriz deve conter uma estrutura para cada par de nome de serviço e nome de tópico que corresponda ao par nome-do-serviço e tópico-nome solicitado pelo cliente. A matriz deve ser terminada por um identificador de cadeia de caracteres **nula** . O sistema envia a transação de [**\_ \_ confirmação do XTYP Connect**](xtyp-connect-confirm.md) para o servidor para confirmar cada conversa e passar os identificadores de conversa para o servidor. O servidor não receberá essas confirmações se tiver especificado o sinalizador **CBF \_ ignorar \_ Connect \_ confirmations** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

O servidor deve retornar **NULL** para recusar a transação **XTYP \_ WILDCONNECT** .

## <a name="remarks"></a>Comentários

Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ Fail \_ Connections** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Um servidor não pode bloquear esse tipo de transação; o \_ código de retorno de bloco CBR é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Ddeml. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

