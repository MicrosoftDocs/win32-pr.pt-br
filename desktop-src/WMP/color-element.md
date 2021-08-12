---
title: Elemento Color
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento Color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Elemento Color Windows Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8576f94c2d1aa88608f8f40cbfe32c2d1dc315e0e4578ca6554fa5fcde82c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580751"
---
# <a name="color-element"></a>Elemento Color

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento Color especifica a cor do plano de fundo dos botões de navegação da loja online, do texto do botão e da barra de tarefas recursos.

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (obrigatório)
</dt> <dd>

Valor de cor RGB hexadecimal. Especifica a cor do plano de fundo dos botões e da barra de tarefas.

</dd> <dt>

<span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (obrigatório)
</dt> <dd>

Valor de cor RGB hexadecimal. Especifica a cor do texto do botão.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

O valor padrão para **MediaPlayer** é \# 7C9AD6. O valor padrão para **MediaPlayerText** é \# FFFFFF.

Certifique-se de usar cores que tornam mais fácil para o usuário ler o texto do botão. Por exemplo, você deve evitar o uso de texto de botão branco em botões de cor clara.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





