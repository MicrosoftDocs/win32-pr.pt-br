---
title: Transação de XTYP_XACT_COMPLETE (ddeml. h)
description: Uma função de retorno de chamada do cliente troca dinâmica de dados (DDE), DdeCallback, recebe a \_ \_ transação de conclusão de transações XTYP quando uma transação assíncrona, iniciada por uma chamada para a função DdeClientTransaction, foi concluída.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- Troca de dados de transação XTYP_XACT_COMPLETE
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
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779870"
---
# <a name="xtyp_xact_complete-transaction"></a>Transação do XTYP \_ \_ Transaction concluída

Uma função de retorno de chamada do cliente troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **\_ \_ conclusão** de transações XTYP quando uma transação assíncrona, iniciada por uma chamada para a função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , foi concluída.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uType* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato dos dados associados à transação concluída (se aplicável) ou **NULL** se nenhum dado foi trocado durante a transação.

</dd> <dt>

*hconv* 
</dt> <dd>

Um identificador para a conversa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Um identificador para o nome do tópico envolvido na transação concluída.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um identificador para o nome do item envolvido na transação concluída.

</dd> <dt>

*hdata* 
</dt> <dd>

Um identificador para os dados envolvidos na transação concluída, se aplicável. Se a transação foi bem-sucedida, mas não envolvia nenhum dado, esse parâmetro é **true**. Esse parâmetro será **nulo** se a transação não tiver sido bem-sucedida.

</dd> <dt>

*dwData1* 
</dt> <dd>

O identificador da transação concluída.

</dd> <dt>

*dwData2* 
</dt> <dd>

Quaisquer sinalizadores de status **DDE \_** aplicáveis na palavra inferior. Esse parâmetro fornece suporte para aplicativos dependentes de bits **\_ APPSTATUS do DDE** . É recomendável que os aplicativos não usem mais esses bits, eles podem não ter suporte em versões futuras do DDEML.

</dd> </dl>

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

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

