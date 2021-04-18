---
title: Elemento HTMLView
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento HTMLView especifica a URL base de uma página da Web HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- Elemento HTMLView do Windows Media Player
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800129"
---
# <a name="htmlview-element"></a>Elemento HTMLView

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **HtmlView** especifica a URL base de uma página da Web HtmlView.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obrigatório)
</dt> <dd>

URL base para a página da Web do HTMLView que o Windows Media Player exibe.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

Você pode usar esse elemento para integrar o recurso HTMLView com sua loja online. Se o domínio da URL especificado pelo repositório online atual corresponder ao da página da Web do HTMLView, a opção de **executar agora** acontece sem intervenção do usuário e o conteúdo de HtmlView é exibido. Caso contrário, o Windows Media Player solicita ao usuário permissão para mostrar o conteúdo do HTMLView.

Por exemplo, se a URL para a página da Web HTMLView for https://www.proseware.com/html/HTMLView.htm e a URL para o atributo **BaseURL** for especificada como https://www.proseware.com , a página da Web HtmlView será exibida sem avisar o usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------|
| Versão<br/> | Windows Media Player 10 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Exibindo páginas da Web no Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





