---
title: XTYP_WILDCONNECT transações (Ddeml.h)
description: Permite que um cliente estabeleça uma conversa em cada um dos pares de nome de serviço e nome do tópico do servidor que corresponderem ao nome do serviço e ao nome do tópico especificados.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- XTYP_WILDCONNECT dados de transação Exchange
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
ms.openlocfilehash: f5b2b170a8d2362dec6311f935a5bc0bb92fa16a9b04270afc59d8fe5ad5c19f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914726"
---
# <a name="xtyp_wildconnect-transaction"></a>Transação XTYP \_ WILDCONNECT

Permite que um cliente estabeleça uma conversa em cada um dos pares de nome de serviço e nome do tópico do servidor que corresponderem ao nome do serviço e ao nome do tópico especificados. Uma função de retorno de chamada do servidor Dados Dinâmicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica um nome de serviço **NULL,** um nome de tópico **NULL** ou ambos em uma chamada para a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) ou [**DdeConnectList.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Utype* 
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

Um handle para o nome do tópico. Se esse parâmetro for **NULL,** o cliente solicitará uma conversa em todos os nomes de tópicos com suporte do servidor.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um alça para o nome do serviço. Se esse parâmetro for **NULL,** o cliente solicitará uma conversa em todos os nomes de serviço aos que o servidor dá suporte.

</dd> <dt>

*hdata* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData1* 
</dt> <dd>

Um ponteiro para uma [**estrutura CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contém informações de contexto para a conversa. Se o cliente não for um aplicativo DDEML, esse parâmetro será definido como 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica se o cliente é a mesma instância de aplicativo que o servidor. Se o parâmetro for 1, o cliente será a mesma instância. Se o parâmetro for 0, o cliente será uma instância diferente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O servidor deve retornar um identificador de dados que identifica uma matriz de [**estruturas HSZPAIR.**](/windows/win32/api/ddeml/ns-ddeml-hszpair) A matriz deve conter uma estrutura para cada par nome-de-serviço e nome do tópico que corresponde ao par nome-do-serviço e nome do tópico solicitado pelo cliente. A matriz deve ser encerrada por um alça de cadeia de caracteres **NULL.** O sistema envia a transação CONFIRM do [**XTYP \_ CONNECT \_**](xtyp-connect-confirm.md) para o servidor para confirmar cada conversa e passar as alças de conversa para o servidor. O servidor não receberá essas confirmações se tiver especificado o sinalizador **CBF \_ SKIP CONNECT \_ \_ CONFIRMS** na [**função DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

O servidor deve retornar **NULL para** recusar a transação **XTYP \_ WILDCONNECT.**

## <a name="remarks"></a>Comentários

Essa transação será filtrada se o aplicativo de servidor especificar o sinalizador **CBF \_ FAIL \_ CONNECTIONS** na [**função DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Um servidor não pode bloquear esse tipo de transação; o código de retorno \_ CBR BLOCK é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



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

**Conceitual**
</dt> <dt>

[biblioteca de Dados Dinâmicos Exchange gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

