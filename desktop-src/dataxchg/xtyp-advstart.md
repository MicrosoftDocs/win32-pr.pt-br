---
title: XTYP_ADVSTART transações (Ddeml.h)
description: Um cliente usa a transação XTYP \_ ADVSTART para estabelecer um loop de consultoria com um servidor.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART dados de transação Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb18bda3dce4db465045991e26cdc2d97ddd87ddc69c494ffaf103c566955da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544755"
---
# <a name="xtyp_advstart-transaction"></a>Transação DE ADVSTART do XTYP \_

Um cliente usa a **transação XTYP \_ ADVSTART** para estabelecer um loop de consultoria com um servidor. Uma função de retorno de chamada do servidor Dados Dinâmicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_ ADVSTART** como o *parâmetro wType* da função [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Utype* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato de dados solicitado pelo cliente.

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

## <a name="return-value"></a>Valor retornado

Uma função de retorno de chamada do servidor deve retornar **TRUE** para permitir um loop de consultoria no nome do tópico e no par de nomes de item especificados ou **FALSE** para negar o loop de consultoria. Se a função de retorno de chamada retornar **TRUE**, quaisquer chamadas subsequentes para a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) pelo servidor no mesmo nome de tópico e par de nomes de item faz com que o sistema envie transações [**\_ ADVREQ XTYP**](xtyp-advreq.md) para o servidor.

## <a name="remarks"></a>Comentários

Se um cliente solicitar um loop de consultoria em um nome de tópico, nome do item e formato de dados para um loop de consultoria que já está estabelecido, a DDEML (Biblioteca de Gerenciamento do Dados Dinâmicos Exchange) não criará um loop de consultoria duplicado, mas, em vez disso, alterará os sinalizadores de loop de consultoria (**XTYPF \_ ACKREQ** e **XTYPF \_ NODATA**) para corresponder à solicitação mais recente.

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

 

