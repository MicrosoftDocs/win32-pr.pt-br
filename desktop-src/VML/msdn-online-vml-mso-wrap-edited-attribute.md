---
title: Atributo VML MSO-Wrap-editado
description: Atributo VML MSO-Wrap-editado
ms.assetid: cb0e8618-e649-4a3c-9433-2be77c4b65f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a272a56b57d82ca0fee9f69fbde2757316439fd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105754296"
---
# <a name="vml-mso-wrap-edited-attribute"></a>Atributo VML MSO-Wrap-editado

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se as coordenadas de encapsulamento foram personalizadas pelo usuário. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* Style = "Die-Wrap-edited: *expression* " >

**Comentários**

Se as coordenadas de encapsulamento forem geradas por um editor, esse atributo será **true**; caso contrário, eles foram personalizados por um usuário.

*Atributo de extensões de Microsoft Office*

**Exemplo**

As coordenadas de quebra automática da forma foram geradas por um editor de forma.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-edited:True"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 