---
title: Elemento ButtonTip
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Elemento ButtonTip do Windows Media Player
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813185"
---
# <a name="buttontip-element"></a>Elemento ButtonTip

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **ButtonTip** especifica a cadeia de caracteres de texto que é exibida quando o usuário aponta para um botão de painel de tarefas.

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento                                              |
|-----------------|------------------------------------------------------|
| Elementos pai | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Elementos filho  | Nenhum                                                 |



 

## <a name="remarks"></a>Comentários

Esse elemento é opcional para cada instância de **ServiceTask1**, **ServiceTask2** ou **ServiceTask3**. Se esse elemento não for fornecido, o Windows Media Player usará o texto do botão como o valor padrão.

> [!Note]  
> O Windows Media Player 10 tem três painéis de tarefas em que um repositório online pode exibir suas páginas da Web. O repositório online pode optar por usar um, dois ou todos os três painéis de tarefas. O Windows Media Player 11 tem apenas um painel de tarefas, que pode ser exibido pelo usuário clicando na guia **lojas online** . o Windows Media Player 11 ignora os elementos **ServiceTask2** e **ServiceTask3** .

 

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

 

 





