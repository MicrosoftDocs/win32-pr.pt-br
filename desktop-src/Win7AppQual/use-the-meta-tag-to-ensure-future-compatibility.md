---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Use a marca meta para garantir a compatibilidade futura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814481"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Use a marca meta para garantir a compatibilidade futura

O Windows Internet Explorer 8 permite que você controle modos de compatibilidade de documentos, para que você possa instruir o navegador a renderizar páginas da Web da mesma forma que as versões mais antigas do navegador. Você também pode escolher quando atualizar a página da Web, enquanto ela continua a ser usada e funciona corretamente.

## <a name="setting-the-meta-element"></a>Configurando o elemento meta

O **meta** Element inclui um atributo **Content** que permite que você especifique o modo no qual o conteúdo é renderizado para a página da Web, como mostra a tabela a seguir.



| Valor | Modo de renderização                                                 |
|-------|----------------------------------------------------------------|
| IE = 9  | Usar o modo de renderização de padrões do Windows Internet Explorer 9   |
| IE = 8  | Usar o modo de renderização de padrões do Internet Explorer 8           |
| IE = 7  | Usar o modo de renderização de padrões do Windows Internet Explorer 7   |
| IE=5  | Usar o modo de renderização de padrões do Microsoft Internet Explorer 5 |



 

Para obter mais informações sobre compatibilidade e o cabeçalho de X-UA-Compatible, consulte [definindo a compatibilidade de documentos](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) na biblioteca MSDN.

O exemplo de código a seguir demonstra como forçar uma página da Web a ser renderizada no modo do Internet Explorer 8.


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a>Usando um cabeçalho HTTP

Muitos sites contêm milhares (ou dezenas de milhares) de páginas da Web individuais, portanto, a definição do elemento **meta** em cada documento não é prática. Se desejar definir o elemento **meta** para todas as páginas ou uma coleção de páginas selecionadas por pasta, você poderá ajustar a configuração do servidor e adicionar os metadados compatíveis com X-UA no [cabeçalho http](/previous-versions/cc817572(v=msdn.10)).

Para sites que exigem valores diferentes de elementos **meta** para páginas no mesmo servidor, há várias ferramentas que geram e inserem automaticamente o elemento **meta** apropriado para você. Por exemplo, o utilitário [A ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) da aggiorno insere e remove o recurso de marca de compatibilidade do Internet Explorer 8 e pode ajudar seu site a atender a padrões de compatibilidade específicos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
