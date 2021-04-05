---
title: Mensagem de EM_SETZOOM (RichEdit. h)
description: Define a taxa de zoom. A proporção deve ser um valor entre 1/64 e 64. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- Controles de EM_SETZOOM de mensagens do Windows
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
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824523"
---
# <a name="em_setzoom-message"></a>\_Mensagem em SETzoom

Define a taxa de zoom para um controle de edição de várias linhas ou um controle de edição rico. A proporção deve ser um valor entre 1/64 e 64. O controle de edição precisa ter o estilo estendido de **s \_ ex \_ zoom** definido, para que essa mensagem tenha um efeito, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Numerador da taxa de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

O denominador da taxa de zoom. Esses parâmetros podem ter os valores a seguir.



| Valor                                                                                                                                                                                                                                                              | Significado                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Ambos 0**</dt> </dl>                                                                                                   | Desativa o zoom usando a mensagem em **\_ setZoom** (o zoom ainda pode ocorrer usando [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | Amplia a exibição pelo numerador/denominador da taxa de zoom<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a nova configuração de zoom for aceita, o valor de retorno será **true**.

Se a nova configuração de zoom não for aceita, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

**Editar:** Com suporte no Windows 10 1809 e posterior. O controle de edição precisa ter o estilo estendido de **s \_ ex \_ zoom** definido, para que essa mensagem tenha um efeito, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md). Para obter informações sobre o controle de edição, consulte [Editar controles](about-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h/commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETzoom**](em-getzoom.md)
</dt> </dl>

 

 





