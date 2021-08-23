---
title: EM_GETCUEBANNER mensagem (Commctrl.h)
description: Obtém o texto exibido como a indicação textual ou dica em um controle de edição.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5a47811adcd13c0f2531bd645a9ea607dd68c4dd2c1154f226a54cf108b291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019714"
---
# <a name="em_getcuebanner-message"></a>Mensagem EM \_ GETCUEBANNER

Obtém o texto exibido como a indicação textual ou dica em um controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

Um ponteiro para um buffer Unicode que recebe o conjunto de texto como a indicação textual. O chamador é responsável por alocar o buffer.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

O tamanho do buffer apontado por *wParam* em **WCHARs,** incluindo o NULL de **terminação.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Editar \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





