---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Cadeia de Caracteres do Agente do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922970"
---
# <a name="user-agent-string"></a>Cadeia de Caracteres do Agente do Usuário

A *cadeia de caracteres do agente do usuário* contém informações sobre a identidade de um navegador. A cadeia de caracteres do agente do usuário é relatada ao servidor Web como um cabeçalho HTTP toda vez que um navegador faz uma solicitação para um servidor Web. Você também pode acessá-lo por meio de um script do lado do cliente. Por exemplo, você pode exibir a cadeia de caracteres do agente do usuário digitando a seguinte URL na barra de endereços do Windows Internet Explorer 8: "JavaScript: Alert (Navigator. UserAgent)". A ilustração a seguir mostra a caixa de diálogo resultante típica do Internet Explorer 8 em execução no Windows 7.

![captura de tela da caixa diaog do Internet Explorer que tem a cadeia de caracteres do agente do usuário](images/useragent-alert.png)

Normalmente, a cadeia de caracteres do agente do usuário é analisada especificamente para a subcadeia de caracteres MSIE. Com base na versão relatada do navegador, a lógica de programação do lado do cliente ou do servidor executa uma ação diferente. Para obter mais informações sobre a cadeia de caracteres do agente do usuário, consulte [o que será o relatório do Windows Internet Explorer como a cadeia de caracteres User-Agent?](/previous-versions/cc817582(v=msdn.10)) na biblioteca MSDN.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



