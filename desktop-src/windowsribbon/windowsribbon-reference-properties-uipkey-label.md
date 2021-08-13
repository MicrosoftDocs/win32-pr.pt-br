---
title: UI_PKEY_Label
description: Identifica a propriedade rótulo \_ PKEY \_ da interface do usuário.
ms.assetid: 4d704133-bba7-4c32-a552-d748b66455eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13506d1609f915c2eab9824a3f5256383c5f2aecf73ed5787e3372f17b44b435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706427"
---
# <a name="ui_pkey_label"></a>Rótulo \_ PKEY da interface do \_ usuário

Identifica a propriedade rótulo \_ PKEY \_ da interface do usuário.

```
propertyDescription
   name = UI_PKEY_Label
   shellPKey = UI_PKEY_Label
   formatID = 00000004-7363-696e-8441798acf5aebb7
   propID = 4
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentários

O rótulo PKEY da interface do usuário é usado por um aplicativo para consultar o texto do rótulo de \_ guias, grupos, botões, itens da galeria e outros controles da Faixa \_ de Opções.

> [!Note]  
> Windows 8 e mais novos: imagem [do botão Menu](windowsribbon-controls-applicationmenu.md) do Aplicativo alterada para rótulo: **Arquivo**. Recomendamos que você não use Arquivo como o rótulo para qualquer uma de suas próprias guias.

 

O valor da propriedade é uma cadeia de caracteres restrita a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.

> [!Note]  
> Use a referência de caractere XML do Conjunto de Caracteres Universal (UCS) `&#xA;` para especificar uma quebra de linha.

 

Não há suporte para o alinhamento à direita.

O comprimento máximo do rótulo PKEY da interface do \_ \_ usuário é ilimitado.

Se um Comando for exposto por meio de um item de menu e o valor de [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) ou rótulo PKEY da interface do usuário contiver uma letra precedida por um e comercial, conforme mostrado no exemplo a seguir, essa letra será tratada como uma dica de tecla e um acelerador de teclado para esse comando pela estrutura \_ \_ ribbon.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Para exibir um e ampersand em um rótulo, escape da designação de caractere especial com um e ampersand duplo ( ), conforme `&&` mostrado no exemplo a seguir.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md)
</dt> <dt>

[IU \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 




