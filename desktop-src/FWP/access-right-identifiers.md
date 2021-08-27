---
title: Identificadores de direito de acesso (Fwpmu. h)
description: Windows A WFP (plataforma de filtragem) usa os direitos de acesso padrão do Win32, além de um conjunto de direitos de acesso específicos de WFP incorporados à plataforma de filtragem.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6deee82b792f525814ac4c841da8a848e4f7b978720755c82f93a9569ba21ca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951371"
---
# <a name="access-right-identifiers"></a>Identificadores de direito de acesso

Windows A WFP (plataforma de filtragem) usa os [direitos de acesso padrão do Win32](/windows/desktop/SecAuthZ/standard-access-rights) , além de um conjunto de direitos de acesso específicos de WFP incorporados à plataforma de filtragem. Esses direitos de acesso são usados para proteger objetos somente no modo de usuário. Os chamadores de modo kernel ignoram todas as verificações de acesso.

Os identificadores corretos de acesso específico à WFP são os seguintes.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**
</dt> <dd> <dl> <dt>



Adicione um objeto ao mecanismo de filtragem base (BFE). Esse direito de acesso é necessário para chamar as funções do [**Fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Add \_ link**
</dt> <dd> <dl> <dt>



Adicione um objeto referenciado por meio de um link. Por exemplo, esse direito de acesso é necessário para textos explicativos referenciados por meio de GUIDs.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ begin \_ Read \_ TXN**
</dt> <dd> <dl> <dt>



Iniciar uma transação somente leitura. Esse direito de acesso é necessário para chamar [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ begin \_ Write \_ TXN**
</dt> <dd> <dl> <dt>



Iniciar uma transação de leitura/gravação. Esse direito de acesso é necessário para chamar [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) para uma transação de leitura/gravação.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ classificar**
</dt> <dd> <dl> <dt>



Classificar RPC (chamada de procedimento remoto). Esse direito de acesso é necessário para o tempo de execução de RPC a fim de impor filtros RPC.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ enum**
</dt> <dd> <dl> <dt>



Enumera. Esse direito de acesso é necessário para chamar as funções do [**Fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) . Para enumerar um objeto, o chamador também precisa \_ de \_ acesso de leitura do FWPM ACTRL ao objeto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**
</dt> <dd> <dl> <dt>



Abra uma sessão para o mecanismo de filtro. Esse direito de acesso é necessário para chamar [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ leitura**
</dt> <dd> <dl> <dt>



Leitura. Esse direito de acesso é necessário para chamar as funções [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) e [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ Read \_ stats**
</dt> <dd> <dl> <dt>



Ler estatísticas. Esse direito de acesso é necessário para chamar [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) e [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ assinatura**
</dt> <dd> <dl> <dt>



Inscrever-se. Esse direito de acesso é necessário para chamar as funções do [**Fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) . Para receber uma notificação de um objeto, um assinante também precisa \_ de \_ acesso de leitura do FWPM ACTRL ao objeto.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**
</dt> <dd> <dl> <dt>



Opções do mecanismo de gravação. Esse direito de acesso é necessário para chamar [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**\_leitura genérica do FWPM \_**
</dt> <dd> <dl> <dt>



STANDARD \_ Rights \_ Read \| FWPM \_ ACTRL \_ begin \_ Read \_ TXN \| FWPM \_ ACTRL \_ classificar \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM ACTRL \_ \_ Read \_ stats


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_execução genérica do FWPM \_**
</dt> <dd> <dl> <dt>



\_direitos padrão \_ Execute \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Subscribe


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**\_gravação genérica \_ FWPM**
</dt> <dd> <dl> <dt>



STANDARD \_ Rights \_ Write \| excluir \| FWPM \_ ACTRL \_ Adicionar \| FWPM \_ ACTRL \_ Adicionar \_ link \| FWPM \_ ACTRL \_ começar \_ gravação \_ TXN \| \_ \_ FWPM ACTRL gravação


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ genérico \_ tudo**
</dt> <dd> <dl> <dt>



\_direitos padrão \_ necessários \| FWPM \_ ACTRL \_ Add \| FWPM \_ ACTRL \_ Add \_ link \| FWPM \_ ACTRL \_ begin \_ Read \_ TXN FWPM ACTRL \| \_ \_ begin \_ Write TXN FWPM ACTRL \_ \| \_ \_ classificar \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ Read \| FWPM \_ ACTRL \_ Read \_ stats FWPM \| \_ ACTRL \_ Subscribe \| \_ \_ FWPM ACTRL Write


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Modelo de controle de acesso à plataforma de filtragem](access-control.md)
</dt> <dt>

[Direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

