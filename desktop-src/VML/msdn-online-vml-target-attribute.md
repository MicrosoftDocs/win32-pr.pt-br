---
title: Atributo de destino VML
description: Atributo de destino VML
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759591"
---
# <a name="vml-target-attribute"></a>Atributo de destino VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um quadro ou uma janela em que uma URL é exibida. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* Target = " *expressão* " >

**Comentários**

O atributo de **destino** é semelhante ao atributo de **destino** HTML padrão de âncoras.

Os valores são:



| Valor      | Descrição                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TargetName | Cadeia de caracteres que contém o nome do quadro ou da janela na qual carregar o documento.                                                                                                                                                                                 |
| \_ficará    | Especifica que o documento vinculado é carregado em uma nova janela em branco. Esta janela não é nomeada.                                                                                                                                                                  |
| \_meio    | A partir do Internet Explorer 6 para Windows XP Service Pack 2, o \_ atributo de mídia é obsoleto e não tem mais suporte. Primeiro, disponível no Internet Explorer 6, esse valor especificou que o documento vinculado deve ser carregado na barra de mídia.                |
| \_primária   | Especifica que o documento vinculado é carregado no pai imediato do documento que contém o link.                                                                                                                                                      |
| \_procurando   | A partir do Internet Explorer 7 para Windows XP Service Pack 2,: o \_ atributo de pesquisa é obsoleto e não tem mais suporte. Primeiro, disponível no Internet Explorer 6, esse valor especificou que o documento vinculado foi carregado no painel de pesquisa do navegador. |
| \_auto-restauração     | Especifica que o documento vinculado é carregado na janela em que o link foi clicado (a janela ativa).                                                                                                                                                  |
| \_Início      | Especifica que o documento vinculado é carregado na janela mais alta.                                                                                                                                                                                            |



 

*Atributo padrão da VML*

**Exemplo**

Quando o retângulo é clicado, o navegador carrega o home page da Microsoft Corporation na mesma janela.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemplo de atributo de destino](/previous-versions/bb264096(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 