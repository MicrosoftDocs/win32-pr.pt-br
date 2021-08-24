---
title: XTYP_ADVREQ transações (Ddeml.h)
description: A transação XTYP ADVREQ informa ao servidor que uma transação de consultoria está pendente no nome do tópico e no par de nomes de item especificados e que os dados correspondentes ao nome do tópico e ao par de nomes de \_ item foram alterados.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ dados da transação Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e751f17fb8634b0a105a36af5036f07d0212532349c267e5526d5d41f09367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544881"
---
# <a name="xtyp_advreq-transaction"></a>Transação do XTYP \_ ADVREQ

A **transação XTYP \_ ADVREQ** informa ao servidor que uma transação de consultoria está pendente no nome do tópico e no par de nomes de item especificados e que os dados correspondentes ao nome do tópico e ao par de nomes de item foram alterados. O sistema envia essa transação para a função de retorno de chamada Dados Dinâmicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), depois que o servidor chama a [**função DdePostAdvise.**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Utype* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato no qual os dados devem ser enviados ao cliente.

</dd> <dt>

*hconv* 
</dt> <dd>

Um alça para a conversa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Um handle para o nome do tópico.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um alça para o nome do item que foi alterado.

</dd> <dt>

*hdata* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData1* 
</dt> <dd>

A contagem, na palavra de ordem baixa, de transações **\_ ADVREQ XTYP** que permanecem a ser processadas no mesmo tópico, item e nome de formato definidos no contexto da chamada atual para a [**função DdePostAdvise.**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) A contagem será zero se a transação **atual do XTYP \_ ADVREQ** for a última. Um servidor pode usar essa contagem para determinar se um lidar com **dados \_ HDATA APPOWNED** deve ser criado para os dados de consultoria.

A palavra de ordem baixa será definida como **CADV \_ LATEACK** se o DDEML emitiu a transação **\_ XTYP ADVREQ** devido a uma mensagem de ACK de DDE de chegada tardia de um cliente que está sendo ultrapassado pelo \_ servidor.

A palavra de ordem alta não é usada.

</dd> <dt>

*dwData2* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O servidor deve primeiro chamar a [**função DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para criar um identificador de dados que identifica os dados alterados e, em seguida, retornar o identificador. O servidor deverá retornar **NULL** se não for possível concluir a transação.

## <a name="remarks"></a>Comentários

Um servidor não pode bloquear esse tipo de transação; o **código de retorno \_ CBR BLOCK** é ignorado.

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

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceitual**
</dt> <dt>

[biblioteca de Dados Dinâmicos Exchange gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

