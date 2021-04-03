---
title: Transação de XTYP_DISCONNECT (ddeml. h)
description: A função de retorno de chamada de troca dinâmica de dados (DDE) de um aplicativo, DdeCallback, recebe a \_ transação de desconexão de XTYP quando o parceiro do aplicativo em uma conversa usa a função DdeDisconnect para encerrar a conversa.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- Troca de dados de transação XTYP_DISCONNECT
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644357"
---
# <a name="xtyp_disconnect-transaction"></a>\_Transação de desconexão de XTYP

A função de retorno de chamada de troca dinâmica de dados (DDE) de um aplicativo, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **\_ desconexão de XTYP** quando o parceiro do aplicativo em uma conversa usa a função [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) para encerrar a conversa.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

Um identificador para que a conversa foi encerrada.

</dd> <dt>

*hsz1* 
</dt> <dd>

Não usado.

</dd> <dt>

*hsz2* 
</dt> <dd>

Não usado.

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

Especifica se os parceiros na conversa são a mesma instância do aplicativo. Se esse parâmetro for 1, os parceiros serão a mesma instância. Se esse parâmetro for 0, os parceiros serão instâncias diferentes.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa transação será filtrada se o aplicativo tiver especificado o sinalizador **CBF \_ ignorar \_ desconexões** na função [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

O aplicativo pode obter o status da conversa encerrada chamando a função [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante o processamento dessa transação. O identificador de conversa se torna inválido depois que a função de retorno de chamada retorna.

Um aplicativo não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado.

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

[**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

**Conceitua**
</dt> <dt>

[troca dinâmica de dados biblioteca de gerenciamento](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

