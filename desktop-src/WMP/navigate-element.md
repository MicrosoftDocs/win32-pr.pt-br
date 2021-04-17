---
title: Elemento Navigate
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento Navigate especifica uma URL usada por chamadas para external. NavigateTaskPaneURL.
ms.assetid: 3898e381-baf8-481a-90ee-d64e55b319a0
keywords:
- Navegar no elemento Windows Media Player
topic_type:
- apiref
api_name:
- Navigate Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab3a76fba522332f1414b02d3e317f2793e88292
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747688"
---
# <a name="navigate-element"></a>Elemento Navigate

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **Navigate** especifica uma URL usada por chamadas para **external. NavigateTaskPaneURL**.

``` syntax
<Navigate
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Atributos



| Termo                                                                                                                                             | Descrição                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obrigatório)<br/> | URL totalmente qualificada para a página da Web na qual navegar. **NavigateTaskPaneURL** pode acrescentar uma cadeia de caracteres de consulta a essa URL.<br/> |



 

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

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

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





