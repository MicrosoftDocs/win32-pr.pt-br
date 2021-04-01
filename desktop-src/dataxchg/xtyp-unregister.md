---
title: Transação de XTYP_UNREGISTER (ddeml. h)
description: Uma função de retorno de chamada de troca dinâmica de dados (DDE), DdeCallback, recebe a \_ transação de CANcelamento de registro XTYP sempre que um aplicativo de servidor de biblioteca de gerenciamento de troca dinâmica de dados (ddeml) usa a função DdeNameService para cancelar o registro de um nome de serviço ou sempre que um aplicativo não ddeml que dá suporte ao tópico do sistema é encerrado.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- Troca de dados de transação XTYP_UNREGISTER
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644992"
---
# <a name="xtyp_unregister-transaction"></a>XTYP \_ Cancelar registro da transação

Uma função de retorno de chamada de troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **\_ cancelamento de registro XTYP** sempre que um aplicativo de servidor de biblioteca de gerenciamento de troca dinâmica de dados (ddeml) usa a função [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para cancelar o registro de um nome de serviço ou sempre que um aplicativo não ddeml que dá suporte ao tópico do sistema é encerrado.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Um identificador para o nome do serviço base que está sendo cancelado.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um identificador para o nome do serviço específico da instância que está sendo cancelado.

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

Essa transação será filtrada se o aplicativo tiver especificado o sinalizador **CBF \_ ignorar \_ registros** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Um aplicativo não pode bloquear esse tipo de transação; o \_ código de retorno de bloco CBR é ignorado.

Um aplicativo deve usar o parâmetro *hsz1* para remover o nome do serviço da lista de servidores disponíveis para o usuário. Um aplicativo deve usar o parâmetro *hsz2* para identificar qual instância de aplicativo foi encerrada.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

