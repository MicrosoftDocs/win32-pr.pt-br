---
title: Mensagem de EM_SEARCHWEB (commctrl. h)
description: Abre o navegador e executa uma pesquisa na Web com o texto selecionado como o termo de pesquisa.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- controles de Windows de mensagem de EM_SEARCHWEB
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21523df67acf91b8a44f59ea40b012f1af7c287185b7ac64b5dc1288005dfb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673172"
---
# <a name="em_searchweb-message"></a>\_Mensagem em SEARCHWEB

Abre o navegador e executa uma pesquisa na Web com o texto selecionado como o termo de pesquisa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Se o recurso "Pesquisar na Web" for desabilitado usando a mensagem em [**\_ ENABLESEARCHWEB**](em-enablesearchweb.md) , essa mensagem não terá nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, 1809 \[ aplicativos de área de trabalho apenas\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2019\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> </dl>

 

 





