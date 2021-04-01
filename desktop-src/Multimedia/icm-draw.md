---
title: Mensagem de ICM_DRAW (VFW. h)
description: A \_ mensagem de desenho ICM notifica um driver de renderização para descompactar um quadro de dados e desenhá-lo na tela.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- Multimídia do Windows de mensagem ICM_DRAW
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
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644567"
---
# <a name="icm_draw-message"></a>Mensagem de desenho de ICM \_

A mensagem de **\_ desenho ICM** notifica um driver de renderização para descompactar um quadro de dados e desenhá-lo na tela.


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

Se você quiser que o driver Descompacte dados em um buffer, envie a mensagem de [**\_ descompactação ICM**](icm-decompress.md) .

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

 

 





