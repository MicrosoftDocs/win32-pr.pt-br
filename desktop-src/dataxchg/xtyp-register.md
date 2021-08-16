---
title: XTYP_REGISTER transações (Ddeml.h)
description: Uma função de retorno de chamada DDE (Dados Dinâmicos Exchange), DdeCallback, recebe o tipo de transação REGISTER XTYP sempre que um aplicativo de servidor DDEML (Biblioteca de Gerenciamento do Dados Dinâmicos Exchange) usa a função DdeNameService para registrar um nome de serviço ou sempre que um aplicativo não DDEML que dá suporte ao tópico Sistema \_ é iniciado.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER dados de transação Exchange
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c4ffdb48b7a69109659e65d816b4ab146a1f38bde976e7f8330746f564bc64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544745"
---
# <a name="xtyp_register-transaction"></a>Transação REGISTER \_ XTYP

Uma função de retorno de chamada DDE (Dados Dinâmicos Exchange), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe o tipo de transação **REGISTER XTYP \_** sempre que um aplicativo de servidor DDEML (Biblioteca de Gerenciamento do Dados Dinâmicos Exchange) usa a função [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar um nome de serviço ou sempre que um aplicativo não DDEML que dá suporte ao tópico System é iniciado.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Utype* 
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

Um handle para o nome do serviço base que está sendo registrado.

</dd> <dt>

*hsz2* 
</dt> <dd>

Um handle para o nome do serviço específico da instância que está sendo registrado.

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

Essa transação será filtrada se o aplicativo especificar o sinalizador **CBF \_ SKIP \_ REGISTRATIONS** na [**função DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Um aplicativo não pode bloquear esse tipo de transação; o **código de retorno \_ CBR BLOCK** é ignorado.

Um aplicativo deve usar o *parâmetro hsz1* para adicionar o nome do serviço à lista de servidores disponíveis para o usuário. Um aplicativo deve usar o *parâmetro hsz2* para identificar qual instância de aplicativo foi iniciada.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Conceitual**
</dt> <dt>

[biblioteca de Dados Dinâmicos Exchange gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

