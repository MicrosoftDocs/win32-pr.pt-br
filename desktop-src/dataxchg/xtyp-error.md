---
title: Transação de XTYP_ERROR (ddeml. h)
description: Uma função de retorno de chamada troca dinâmica de dados (DDE), DdeCallback, recebe a \_ transação de erro XTYP quando ocorre um erro crítico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- Troca de dados de transação XTYP_ERROR
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
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105791496"
---
# <a name="xtyp_error-transaction"></a>\_Transação de erro XTYP

Uma função de retorno de chamada troca dinâmica de dados (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recebe a transação de **\_ erro XTYP** quando ocorre um erro crítico.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
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

Um identificador para a conversa associada ao erro. Esse parâmetro será **nulo** se o erro não estiver associado a uma conversa.

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

O código de erro na palavra de ordem inferior. Atualmente, há suporte apenas para o código de erro a seguir.



| Valor                                                                                                                                                                      | Significado                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**\_memória insuficiente do DMLERR \_**</dt> </dl> | A memória é baixa; aconselhar, examinar ou executar dados podem ser perdidos ou o sistema pode falhar.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um aplicativo não pode bloquear esse tipo de transação; o código de retorno de **\_ bloco CBR** é ignorado. A biblioteca de gerenciamento de troca dinâmica de dados (DDEML) tenta liberar memória removendo recursos não críticos. Um aplicativo que tenha conversas bloqueadas deve desbloqueá-las.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Ddeml. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral da biblioteca de gerenciamento de troca dinâmica de dados](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

