---
title: Elemento Description
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento Description
ms.assetid: 4d9ff447-e5a4-46b1-b599-87202077abfb
keywords:
- Elemento de descrição Windows Media Player
topic_type:
- apiref
api_name:
- Description Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4318a7936f4713d3ff89a2fa73731eea0cdd97db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794490"
---
# <a name="description-element"></a>Elemento Description

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **Description** especifica uma descrição de marketing da loja online que é exibida durante a primeira experiência do usuário com uma instalação do Windows Media Player.

``` syntax
<Description>
    text string
</Description>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento         |
|-----------------|-----------------|
| Elementos pai | **ServiceInfo** |
| Elementos filho  | Nenhum            |



 

## <a name="remarks"></a>Comentários

O comprimento da descrição deve ser menor ou igual a 255 caracteres.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Documento de informações de exemplo para uma loja online tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento de informações de exemplo para uma loja online tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento do serviceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





