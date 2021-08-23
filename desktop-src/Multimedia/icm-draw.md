---
title: Mensagem de ICM_DRAW (VFW. h)
description: o ICM \_ mensagem de desenho notifica um driver de renderização para descompactar um quadro de dados e desenhá-lo na tela.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- mensagem de ICM_DRAW Windows multimídia
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e44216e523da62e0dde22abed8d88b9b8aacd8f68119a88f3177f45ecd910029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784986"
---
# <a name="icm_draw-message"></a>ICM \_ DESENHAR mensagem

o **ICM \_** mensagem de desenho notifica um driver de renderização para descompactar um quadro de dados e desenhá-lo na tela.


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Ponteiro para uma estrutura [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Tamanho, em bytes, de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Se o \_ sinalizador de atualização ICDRAW estiver definido no membro **dwFlags** de [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), a área da tela usada para desenhar será inválida e precisará ser atualizada. A extensão da atualização depende do conteúdo do membro **lpData** .

Se **lpData** for **nulo**, o driver deverá atualizar o retângulo de destino inteiro com a imagem atual. Se o driver mantiver uma cópia da imagem em um buffer fora da tela, ele poderá falhar essa mensagem. Se **lpData** não for **NULL**, o driver deverá desenhar os dados e verificar se o destino inteiro foi atualizado.

Se o \_ sinalizador ICDRAW HURRYUP for definido em **dwFlags**, o aplicativo de chamada deseja que o driver prossiga o mais rápido possível, possivelmente nem mesmo atualizando a tela.

Se o \_ sinalizador de PREROLL ICDRAW estiver definido em **dwFlags**, este quadro de vídeo será informações preliminares e não deverá ser exibido, se possível. Por exemplo, se Play for iniciar do quadro 10 e o quadro 0 for o quadro-chave anterior mais próximo, os quadros de 0 a 9 terão o ICDRAW \_ PRErolled set.

se você quiser que o driver descompacte dados em um buffer, envie a mensagem [**ICM \_ descompactar**](icm-decompress.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





