---
title: Elemento ButtonText
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento ButtonText
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Elemento ButtonText do Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794504"
---
# <a name="buttontext-element"></a>Elemento ButtonText

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O elemento **ButtonText** especifica a cadeia de texto que o Windows Media Player exibe para um botão de painel de tarefas.

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a>Atributos

Esse elemento não tem atributos.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elemento                                              |
|-----------------|------------------------------------------------------|
| Elementos pai | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Elementos filho  | Nenhum                                                 |



 

## <a name="remarks"></a>Comentários

Esse elemento é necessário para cada instância de **ServiceTask1**, **ServiceTask2** ou **ServiceTask3**.

> [!Note]  
> O Windows Media Player 10 tem três painéis de tarefas em que um repositório online pode exibir suas páginas da Web. O repositório online pode optar por usar um, dois ou todos os três painéis de tarefas. O Windows Media Player 11 tem apenas um painel de tarefas, que pode ser exibido pelo usuário clicando na guia **lojas online** . o Windows Media Player 11 ignora os elementos **ServiceTask2** e **ServiceTask3** .

 

O Windows Media Player pode cortar o texto do botão para se ajustar ao espaço disponível. O Player sempre usa a fonte de 8 pontos em negrito Tahoma para esse texto. Há duas linhas disponíveis para exibir o texto do botão, mas o Player não quebra automaticamente o texto da primeira linha para a segunda. Para especificar uma quebra de linha no texto do botão, insira a nova sequência de escape de linha " \\ n" em sua cadeia de texto.

A cadeia de texto também é exibida no menu **ir** na interface de usuário do Windows Media Player.

Você deve testar sua loja online usando uma variedade de configurações de exibição para garantir que o texto seja exibido conforme o esperado.

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

 

 





