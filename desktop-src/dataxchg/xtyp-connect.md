---
title: Transação de XTYP_CONNECT (ddeml. h)
description: Um cliente usa a \_ transação XTYP Connect para estabelecer uma conversa.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- Troca de dados de transação XTYP_CONNECT
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085688"
---
# <a name="xtyp_connect-transaction"></a>Transação do XTYP \_ Connect

Um cliente usa a transação **XTYP \_ Connect** para estabelecer uma conversa. Uma função de retorno de chamada de servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe essa transação quando um cliente especifica um nome de serviço ao qual o servidor dá suporte (e um nome de tópico que não é **nulo**) em uma chamada para a função [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uType* 
</dt> <dd>

O tipo de transação.

</dd> <dt>

*uFmt* 
</dt> <dd>

Não usado.

</dd> <dt>

*hconv* 
</dt> <dd>

Não usado.

</dd> <dt>

*hsz1* 
</dt> <dd>

Um identificador para o nome do tópico.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um identificador para o nome do serviço.

</dd> <dt>

*hdata* 
</dt> <dd>

Não usado.

</dd> <dt>

*dwData1* 
</dt> <dd>

Um ponteiro para uma estrutura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contém informações de contexto para a conversa. Se o cliente não for um aplicativo DDEML, esse parâmetro será 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica se o cliente é a mesma instância de aplicativo que o servidor. Se o parâmetro for 1, o cliente será a mesma instância. Se o parâmetro for 0, o cliente será uma instância diferente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma função de retorno de chamada de servidor deve retornar **true** para permitir que o cliente estabeleça uma conversa no nome do serviço especificado e no par do nome do tópico, ou a função deve retornar **false** para negar a conversa. Se a função de retorno de chamada retornar **true** e uma conversa for estabelecida com êxito, o sistema passará o identificador de conversa para o servidor emitindo uma transação [**XTYP \_ Connect \_ Confirm**](xtyp-connect-confirm.md) para a função de retorno de chamada do servidor (a menos que o servidor tenha especificado o sinalizador **CBF \_ Skip \_ Connect \_ confirmations** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).

## <a name="remarks"></a>Comentários

Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ Fail \_ Connections** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

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

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

