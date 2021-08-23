---
title: Mensagem de EM_SETELLIPSISMODE (RichEdit. h)
description: Essa mensagem define o modo de reticências atual.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- controles de Windows de mensagem de EM_SETELLIPSISMODE
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445172ea0a4ed4ef49e9a131db8d4357faaa5f7fef553169b7a8e1e795fd01c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019474"
---
# <a name="em_setellipsismode-message"></a>\_Mensagem em setreticências

Essa mensagem define o modo de reticências atual. Quando habilitado, uma reticências () é exibida para texto que não se encaixa na janela de exibição. As reticências só são usadas quando o controle não está ativo. Quando ativas, as barras de rolagem são usadas para revelar texto que não se encaixa na janela de exibição.


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um DWORD que recebe um dos valores a seguir.



| Valor                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <dt>**RETICÊNCIAs \_ None**</dt> </dl> | Nenhuma elipse é usada.<br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <dt>**fim da elipse \_**</dt> </dl>    | Reticências no final (quebra forçada).<br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <dt>**palavra de RETICÊNCIAs \_**</dt> </dl> | Reticências no final (quebra de palavra).<br/>   |



 

Todos os bits para esses valores se encaixam na **\_ máscara de reticências**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se wParam for 0 e lParam for um dos valores na tabela acima, o valor de retorno será igual a TRUE; caso contrário, o valor de retorno será igual a falso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETreticênciamode**](em-getellipsismode.md)
</dt> <dt>

[**em \_ getreticências**](em-getellipsisstate.md)
</dt> </dl>

 

 





