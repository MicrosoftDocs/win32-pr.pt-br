---
title: XTYP_CONNECT_CONFIRM transações (Ddeml.h)
description: Uma função de retorno de chamada do servidor Dados Dinâmicos Exchange (DDE), DdeCallback, recebe a transação CONFIRM do XTYP CONNECT para confirmar que uma conversa foi estabelecida com um cliente e fornecer ao servidor o controle de \_ \_ conversa.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- XTYP_CONNECT_CONFIRM dados de transação Exchange
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0259540801a49bc631dc60e33979a8730b46bdfc06ac81142098e851b8a51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499068"
---
# <a name="xtyp_connect_confirm-transaction"></a>XTYP \_ CONNECT \_ CONFIRM transaction

Uma função de retorno de chamada do servidor Dados Dinâmicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação CONFIRM do **XTYP \_ CONNECT \_** para confirmar que uma conversa foi estabelecida com um cliente e fornecer ao servidor o controle de conversa. O sistema envia essa transação como resultado de uma transação [**XTYP \_ CONNECT**](xtyp-connect.md) ou [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) anterior.


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Um alça para a nova conversa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Um handle para o nome do tópico no qual a conversa foi estabelecida.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um handle para o nome do serviço no qual a conversa foi estabelecida.

</dd> <dt>

*hdata* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData1* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica se o cliente é a mesma instância de aplicativo que o servidor. Se o parâmetro for 1, o cliente será a mesma instância. Se o parâmetro for 0, o cliente será uma instância diferente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ SKIP CONNECT \_ \_ CONFIRMS** na [**função DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

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

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Conceitual**
</dt> <dt>

[biblioteca de Dados Dinâmicos Exchange gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

