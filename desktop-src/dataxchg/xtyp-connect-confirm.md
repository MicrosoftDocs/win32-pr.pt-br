---
title: Transação de XTYP_CONNECT_CONFIRM (ddeml. h)
description: Uma função de retorno de chamada do servidor troca dinâmica de dados (DDE), DdeCallback, recebe a transação de confirmação do XTYP \_ Connect \_ para confirmar que uma conversa foi estabelecida com um cliente e para fornecer ao servidor o identificador de conversa.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- Troca de dados de transação XTYP_CONNECT_CONFIRM
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
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369676"
---
# <a name="xtyp_connect_confirm-transaction"></a>\_ \_ Confirmar transação do XTYP Connect

Uma função de retorno de chamada do servidor troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **confirmação do XTYP \_ Connect \_** para confirmar que uma conversa foi estabelecida com um cliente e para fornecer ao servidor o identificador de conversa. O sistema envia essa transação como resultado de uma transação [**XTYP \_ Connect**](xtyp-connect.md) ou [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) anterior.


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Um identificador para a nova conversa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Um identificador para o nome do tópico no qual a conversa foi estabelecida.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um identificador para o nome do serviço no qual a conversa foi estabelecida.

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

Essa transação será filtrada se o aplicativo de servidor tiver especificado o sinalizador **CBF \_ Skip \_ Connect \_ confirmations** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Um servidor não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.

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

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

