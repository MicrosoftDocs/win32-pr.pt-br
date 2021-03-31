---
title: Transação de XTYP_ADVSTART (ddeml. h)
description: Um cliente usa a \_ transação XTYP ADVSTART para estabelecer um loop de aviso com um servidor.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- Troca de dados de transação XTYP_ADVSTART
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
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644739"
---
# <a name="xtyp_advstart-transaction"></a>\_Transação XTYP ADVSTART

Um cliente usa a transação **XTYP \_ ADVSTART** para estabelecer um loop de aviso com um servidor. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica **XTYP \_ ADVSTART** como o parâmetro *wType* da função [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uType* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

O formato de dados solicitado pelo cliente.

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

## <a name="return-value"></a>Retornar valor

Uma função de retorno de chamada de servidor deve retornar **true** para permitir um loop de aviso no nome do tópico e no par do nome do item especificados, ou **false** para negar o loop de aviso. Se a função de retorno de chamada retornar **true**, todas as chamadas subsequentes para a função [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) pelo servidor no mesmo nome de tópico e par de nome de item fazem com que o sistema envie transações [**XTYP \_ ADVREQ**](xtyp-advreq.md) para o servidor.

## <a name="remarks"></a>Comentários

Se um cliente solicitar um loop de aviso em um nome de tópico, nome de item e formato de dados para um loop de aviso que já esteja estabelecido, a troca dinâmica de dados biblioteca de gerenciamento (DDEML) não criará um loop de aviso duplicado, mas, em vez disso, alterará os sinalizadores de loop de aviso (**XTYPF \_ ACKREQ** e **XTYPF \_ NODATA**) para corresponder à solicitação mais recente.

Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF de \_ \_ aviso de falha** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Ddeml. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

