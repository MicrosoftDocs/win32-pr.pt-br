---
title: EM_SETZOOM mensagem (Richedit.h)
description: Define a taxa de zoom. A taxa deve ser um valor entre 1/64 e 64. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf6541bc018df253a3ed45f8bced42e2f19938449d7fc35bf7f309909d53a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437176"
---
# <a name="em_setzoom-message"></a>Mensagem EM \_ SETZOOM

Define a taxa de zoom para um controle de edição multilinha ou um controle de edição rico. A taxa deve ser um valor entre 1/64 e 64. O controle de edição precisa ter o estilo estendido **\_ ES EX \_ ZOOMABLE** definido, para que essa mensagem tenha um efeito, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Numerador da taxa de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Denominador da taxa de zoom. Esses parâmetros podem ter os seguintes valores.



| Valor                                                                                                                                                                                                                                                              | Significado                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Ambos 0**</dt> </dl>                                                                                                   | Desliga o zoom usando a mensagem **EM \_ SETZOOM** (o zoom ainda pode ocorrer usando [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | Amplia a exibição pelo numerador/denominador da taxa de zoom<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a nova configuração de zoom for aceita, o valor de retorno será **TRUE.**

Se a nova configuração de zoom não for aceita, o valor de retorno será **FALSE.**

## <a name="remarks"></a>Comentários

**Editar:** Com suporte no Windows 10 1809 e posterior. O controle de edição precisa ter o estilo estendido **\_ ES EX \_ ZOOMABLE** definido, para que essa mensagem tenha um efeito, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md). Para obter informações sobre o controle de edição, consulte [Editar controles](about-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Redistribuível<br/>          | Rich Edit 3.0<br/>                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h/Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETZOOM**](em-getzoom.md)
</dt> </dl>

 

 





