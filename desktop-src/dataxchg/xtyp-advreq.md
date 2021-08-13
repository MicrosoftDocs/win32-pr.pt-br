---
title: Transação de XTYP_ADVREQ (ddeml. h)
description: A \_ transação XTYP ADVREQ informa ao servidor que uma transação de aviso está pendente no nome do tópico e no par do nome do item especificados e que os dados correspondentes ao nome do tópico e ao par do nome do item foram alterados.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- XTYP_ADVREQ de dados de transação Exchange
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
# <a name="xtyp_advreq-transaction"></a>\_Transação XTYP ADVREQ

A transação **XTYP \_ ADVREQ** informa ao servidor que uma transação de aviso está pendente no nome do tópico e no par do nome do item especificados e que os dados correspondentes ao nome do tópico e ao par do nome do item foram alterados. o sistema envia essa transação para a função de retorno de chamada troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), depois que o servidor chama a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uType* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato no qual os dados devem ser enviados ao cliente.

</dd> <dt>

*hconv* 
</dt> <dd>

Um identificador para a conversa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Um identificador para o nome do tópico.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um identificador para o nome do item que foi alterado.

</dd> <dt>

*hdata* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData1* 
</dt> <dd>

A contagem, na palavra de ordem inferior, das transações **XTYP \_ ADVREQ** que permanecem para ser processada no mesmo tópico, item e nome de formato definido no contexto da chamada atual para a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) . A contagem será zero se a transação **XTYP \_ ADVREQ** atual for a última. Um servidor pode usar essa contagem para determinar se deve criar um identificador de dados **HDATA \_ APPOWNED** para os dados de aviso.

A palavra de ordem inferior é definida como **CADV \_ LATEACK** se o ddeml emitiu a transação **\_ ADVREQ do XTYP** devido a uma mensagem de ACK DDE de chegada \_ de um cliente que está sendo OutRun pelo servidor.

A palavra de ordem superior não é usada.

</dd> <dt>

*dwData2* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O servidor deve primeiro chamar a função [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para criar um identificador de dados que identifica os dados alterados e, em seguida, retornar o identificador. O servidor deverá retornar **NULL** se não for possível concluir a transação.

## <a name="remarks"></a>Comentários

Um servidor não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.

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

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

