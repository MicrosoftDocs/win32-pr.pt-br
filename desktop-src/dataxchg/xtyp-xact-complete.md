---
title: XTYP_XACT_COMPLETE transações (Ddeml.h)
description: Uma função de retorno de chamada do cliente Dados Dinâmicos Exchange (DDE), DdeCallback, recebe a transação XTYP XACT COMPLETE quando uma transação assíncrona, iniciada por uma chamada para \_ \_ a função DdeClientTransaction, é concluída.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE dados da transação Exchange
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3833207371bbfab059f67ecb5bdb72b77334ef3ffc73618e013ce137835c6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678006"
---
# <a name="xtyp_xact_complete-transaction"></a>Transação XTYP \_ XACT \_ COMPLETE

Uma função de retorno de chamada do cliente Dados Dinâmicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação **\_ XTYP XACT \_ COMPLETE** quando uma transação assíncrona, iniciada por uma chamada para a [**função DdeClientTransaction,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) é concluída.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Utype* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato dos dados associados à transação concluída (se aplicável) ou **NULL** se nenhum dado tiver sido trocado durante a transação.

</dd> <dt>

*hconv* 
</dt> <dd>

Um alça para a conversa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Um handle para o nome do tópico envolvido na transação concluída.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um handle para o nome do item envolvido na transação concluída.

</dd> <dt>

*hdata* 
</dt> <dd>

Um lidar com os dados envolvidos na transação concluída, se aplicável. Se a transação tiver sido bem-sucedida, mas não envolver dados, esse parâmetro será **TRUE.** Esse parâmetro será **NULL se** a transação não tiver sido bem-sucedida.

</dd> <dt>

*dwData1* 
</dt> <dd>

O identificador de transação da transação concluída.

</dd> <dt>

*dwData2* 
</dt> <dd>

Qualquer sinalizador de status **DDE \_** aplicável na palavra baixa. Esse parâmetro fornece suporte para aplicativos dependentes de bits **\_ APPSTATUS de DDE.** É recomendável que os aplicativos não usem mais esses bits que talvez não sejam suportados em versões futuras do DDEML.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um aplicativo não deve liberar o handle de dados obtido durante essa transação. No entanto, um aplicativo deve copiar os dados associados ao lidar com os dados se o aplicativo deve processar os dados depois que a função de retorno de chamada retorna. Um aplicativo pode usar a [**função DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar os dados.

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

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**Conceitual**
</dt> <dt>

[biblioteca de Dados Dinâmicos Exchange gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

