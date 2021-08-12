---
title: Transação de XTYP_ADVDATA (ddeml. h)
description: Informa ao cliente que o valor do item de dados foi alterado. a função de retorno de chamada do cliente troca dinâmica de dados (DDE), DdeCallback, recebe essa transação depois de estabelecer um loop de aviso com um servidor.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA de dados de transação Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bf3f3b94f4454547d987ab6536929d1fe2998e7dc0394564143536f1da28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544861"
---
# <a name="xtyp_advdata-transaction"></a>\_Transação XTYP ADVDATA

Informa ao cliente que o valor do item de dados foi alterado. a função de retorno de chamada do cliente troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação depois de estabelecer um loop de aviso com um servidor.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uType* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato Atom dos dados enviados do servidor.

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

Um identificador para o nome do item.

</dd> <dt>

*hdata* 
</dt> <dd>

Um identificador para os dados associados ao nome do tópico e ao par do nome do item. Esse parâmetro será **nulo** se o cliente tiver especificado o sinalizador **\_ NODATA do XTYPF** quando solicitou o loop de aviso.

</dd> <dt>

*dwData1* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData2* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma função de retorno de chamada DDE deve retornar **\_ FACK DDE** se ele processar essa transação, o **DDE \_ FBUSY** se estiver muito ocupado para processar essa transação ou o **DDE \_ FNOTPROCESSED** se rejeitar essa transação.

## <a name="remarks"></a>Comentários

Um aplicativo não deve liberar o identificador de dados obtido durante essa transação. No entanto, um aplicativo deve copiar os dados associados ao identificador de dados se o aplicativo precisar processar os dados depois que a função de retorno de chamada retornar. Um aplicativo pode usar a função [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar os dados.

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

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

