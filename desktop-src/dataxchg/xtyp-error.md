---
title: XTYP_ERROR transações (Ddeml.h)
description: Uma função de retorno de chamada Dados Dinâmicos Exchange (DDE), DdeCallback, recebe a transação XTYP ERROR quando \_ ocorre um erro crítico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR dados da transação Exchange
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce59800723758201b4857b5a3ae0844675347b2d4fd403c77650b36d9275bfb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755976"
---
# <a name="xtyp_error-transaction"></a>Transação de ERRO \_ XTYP

Uma função Dados Dinâmicos Exchange retorno de chamada (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação **XTYP \_ ERROR** quando ocorre um erro crítico.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
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

Um alça para a conversa associada ao erro. Esse parâmetro será **NULL** se o erro não estiver associado a uma conversa.

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

O código de erro na palavra de ordem baixa. Atualmente, há suporte apenas para o código de erro a seguir.



| Valor                                                                                                                                                                      | Significado                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**MEMÓRIA BAIXA DO DMLERR \_ \_**</dt> </dl> | A memória está baixa; os dados de consultoria, de adoção ou execução podem ser perdidos ou o sistema pode falhar.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um aplicativo não pode bloquear esse tipo de transação; o **código de retorno \_ CBR BLOCK** é ignorado. O Dados Dinâmicos Exchange DDEML (Biblioteca de Gerenciamento de Dados) tenta liberar memória removendo recursos nãocríticos. Um aplicativo que bloqueou conversas deve desbloqueá-las.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral Dados Dinâmicos Exchange biblioteca de gerenciamento do Dados Dinâmicos Exchange](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

