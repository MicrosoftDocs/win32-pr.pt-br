---
title: XTYP_POKE transações (Ddeml.h)
description: Um cliente usa a transação XTYP \_ TRANSACTION para enviar dados não solicitados para o servidor. Uma função de retorno de chamada do servidor Dados Dinâmicos Exchange (DDE), DdeCallback, recebe essa transação quando um cliente especifica XTYP DNS na \_ função DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE dados da transação Exchange
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a179f4130ae06c4548b52586d6086201c2d832a158cef877d9aaf524160f4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914746"
---
# <a name="xtyp_poke-transaction"></a>Transação \_ XTYP?

Um cliente usa a **transação XTYP \_ TRANSACTION** para enviar dados não solicitados para o servidor. Uma função de retorno de chamada do servidor Dados Dinâmicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_ DNS** na [**função DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Utype* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato dos dados enviados do servidor.

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

Um handle para os dados que o cliente está enviando para o servidor.

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

Uma função de retorno de chamada do servidor deverá retornar o sinalizador **\_ FACK** de DDE se processar essa transação, o sinalizador **\_ DDE FBUSY** se ele estiver muito ocupado para processar essa transação ou o sinalizador **\_ DDE FNOTPROCESSED** se ela rejeitar essa transação.

## <a name="remarks"></a>Comentários

Essa transação será filtrada se o aplicativo de servidor especificar o sinalizador **CBF \_ \_ FAILESES** na [**função DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

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

**Conceitual**
</dt> <dt>

[biblioteca de Dados Dinâmicos Exchange gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

