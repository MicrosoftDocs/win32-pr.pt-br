---
title: XTYP_ADVSTOP transações (Ddeml.h)
description: Um cliente usa a transação ADVSTOP XTYP \_ para encerrar um loop de consultoria com um servidor. Uma função de retorno de chamada do servidor Dados Dinâmicos Exchange (DDE), DdeCallback, recebe essa transação quando um cliente especifica XTYP \_ ADVSTOP na função DdeClientTransaction.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP dados de transação Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81f1fe407186410e604a259f6e8039c074da039fc23b2f8a090c34ff58154
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544765"
---
# <a name="xtyp_advstop-transaction"></a>Transação DO XTYP \_ ADVSTOP

Um cliente usa a **transação \_ ADVSTOP XTYP** para encerrar um loop de consultoria com um servidor. Uma função de retorno de chamada do servidor Dados Dinâmicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_ ADVSTOP** na [**função DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Utype* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato de dados associado ao loop de consultoria que está sendo encerrado.

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

Um alça para o nome do item.

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

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa transação será filtrada se o aplicativo de servidor especificar o sinalizador **CBF \_ FAIL \_ ADVISES** na [**função DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceitual**
</dt> <dt>

[biblioteca de Dados Dinâmicos Exchange gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

