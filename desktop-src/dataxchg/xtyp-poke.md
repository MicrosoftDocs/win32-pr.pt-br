---
title: Transação de XTYP_POKE (ddeml. h)
description: Um cliente usa a transação XTYP de \_ envio para enviar dados não solicitados ao servidor. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), DdeCallback, recebe essa transação quando um cliente especifica XTYP para \_ a função DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- Troca de dados de transação XTYP_POKE
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
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918360"
---
# <a name="xtyp_poke-transaction"></a>Transação de XTYP \_

Um cliente usa a **transação \_ XTYP** de envio para enviar dados não solicitados ao servidor. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_** para a função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uType* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato dos dados enviados do servidor.

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

Um identificador para os dados que o cliente está enviando para o servidor.

</dd> <dt>

*dwData1* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData2* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma função de retorno de chamada de servidor deve retornar o sinalizador **\_ FACK do DDE** se ele processar essa transação, o sinalizador **DDE \_ FBUSY** se estiver muito ocupado para processar essa transação ou o sinalizador **DDE \_ FNOTPROCESSED** se rejeitar essa transação.

## <a name="remarks"></a>Comentários

Essa transação é filtrada se o aplicativo de servidor especificou o sinalizador **CBF \_ \_ Fail reprovations** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

