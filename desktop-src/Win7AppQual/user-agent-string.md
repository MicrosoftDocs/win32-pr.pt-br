---
description: Cadeia de Caracteres do Agente do Usuário
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Cadeia de Caracteres do Agente do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a4d918845fe317ef64569cde7ef79c7bb1461bcd0205a5ef74daf55b2c0186
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328687"
---
# <a name="user-agent-string"></a>Cadeia de Caracteres do Agente do Usuário

A *cadeia de caracteres do agente do usuário* contém informações sobre a identidade de um navegador. A cadeia de caracteres do agente do usuário é relatada ao servidor Web como um cabeçalho HTTP toda vez que um navegador faz uma solicitação para um servidor Web. Você também pode acessá-lo por meio de um script do lado do cliente. por exemplo, você pode exibir a cadeia de caracteres do agente do usuário digitando a seguinte URL na barra de endereços do Windows Internet Explorer 8: "javascript: alert (navigator. useragent)". a ilustração a seguir mostra a caixa de diálogo resultante típica do Internet Explorer 8 em execução no Windows 7.

![captura de tela da caixa diaog do Internet Explorer que tem a cadeia de caracteres do agente do usuário](images/useragent-alert.png)

Normalmente, a cadeia de caracteres do agente do usuário é analisada especificamente para a subcadeia de caracteres MSIE. Com base na versão relatada do navegador, a lógica de programação do lado do cliente ou do servidor executa uma ação diferente. para obter mais informações sobre a cadeia de caracteres do agente do usuário, consulte [o que será Windows relatório do Internet Explorer como User-Agent cadeia de caracteres?](/previous-versions/cc817582(v=msdn.10)) no Biblioteca MSDN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



