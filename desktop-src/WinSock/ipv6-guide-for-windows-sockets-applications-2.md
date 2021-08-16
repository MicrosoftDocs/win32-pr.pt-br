---
description: Este guia fornece as informações necessárias para permitir que seu aplicativo microsoft Windows use a próxima geração do Protocolo IPv6, versão 6.
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guia IPv6 para aplicativos Windows soquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c52d86dfcdfa06df80dc71a3f3313de19f9201c7421a3f27f094589a6656dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741110"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>Guia IPv6 para aplicativos Windows soquetes

Este guia fornece as informações necessárias para permitir que seu aplicativo microsoft Windows use a próxima geração do Protocolo IPv6, versão 6. Adicionar a funcionalidade IPv6 ao seu aplicativo não é necessariamente um processo de portação. A portabilidade de um aplicativo sugere modificar o código para funcionar em uma plataforma diferente, o que implica deixar a plataforma anterior para trás. Este guia é especificamente estruturado para ajudar a adicionar a funcionalidade IPv6 a um aplicativo, mantendo a funcionalidade IPv4.

Este guia aborda os problemas associados à adição da funcionalidade IPv6 e, em seguida, tem como alvo as áreas de desenvolvimento mais afetadas pela transição. Cada área recebe uma explicação completa das armadilhas a observar, as estratégias sugeridas para evitá-las e dicas sobre como fazer o melhor uso dos novos elementos [programáticos do Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funções e estruturas). Para obter informações adicionais sobre IPv6, consulte [Suporte a IPv6.](ipv6-support-2.md)

Este guia também fornece exemplos de código para lhe dar experiência prática e representações visuais dos problemas que você pode encontrar ao modificar seus aplicativos. Os exemplos vêm de exemplos completos de um aplicativo Windows Sockets simples que foi modificado para dar suporte a IPv4 e IPv6. O código-fonte para esses exemplos de trabalho está incluído em sua totalidade em dois apêndices no final deste documento: [Apêndice A: Código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md) inclui o código-fonte de um aplicativo antes de ser modificado para dar suporte a IPv6; [Apêndice B: o Código-fonte Agnostic](appendix-b-ip-version-agnostic-source-code-2.md) da versão IP fornece o código-fonte depois que o aplicativo tiver sido habilitado para IPv6.

A Microsoft fornece um utilitário chamado Checkv4.exe que ajuda você a encontrar código potencialmente sensível à portação no código do aplicativo e também faz recomendações para correções. O Checkv4.exe utilitário é demonstrado neste documento, usando o aplicativo de exemplo incluído nos apêndices, juntamente com capturas de tela exibindo a saída que o utilitário Checkv4.exe produz. Para obter mais informações, [consulte Usando o utilitário Checkv4.exe .](using-the-checkv4-exe-utility-2.md)

As áreas de programação abordadas por este guia são:

-   [Alterando estruturas de dados para aplicativos Winsock IPv6](changing-data-structures-2.md)
-   [Chamadas de função para aplicativos Winsock IPv6](function-calls-2.md)
-   [Uso de endereços IPv4 em código](use-of-hardcoded-ipv4-addresses-2.md)
-   [Interface do Usuário problemas para aplicativos Winsock IPv6](user-interface-issues-2.md)
-   [Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
-   [Soquetes de pilha dupla para aplicativos Winsock IPv6](dual-stack-sockets.md)

Como não há nenhuma sequência uniforme de eventos, as seções que abordam problemas de habilitação de IPv6 não são organizadas de maneira sequencialmente significativa, portanto, você pode referenciar qualquer seção a qualquer momento. É altamente recomendável que você revise cada seção ao adicionar o recurso IPv6 ao seu aplicativo. Também é aconselhável ler sobre o utilitário Checkv4.exe, pois ele inclui dicas sobre a ordem na qual resolver problemas de habilitação de IPv6.

Para analisar o utilitário Checkv4.exe e analisar a ordem na qual você deve abordar o processo de portação em seus aplicativos, consulte Usando o [utilitário Checkv4.exe .](using-the-checkv4-exe-utility-2.md) Esta seção inclui informações sobre um sinalizador de tempo de compilação que verifica estritamente se há elementos de programação incompatíveis com IPv6.

Para ir diretamente para o aplicativo de exemplo, consulte Apêndice [A: Código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md) e Apêndice [B: Código-fonte Agnostic da](appendix-b-ip-version-agnostic-source-code-2.md)versão IP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IPv6 (Internet Protocol Versão 6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Suporte a IPv6](ipv6-support-2.md)
</dt> <dt>

[Versão prévia da tecnologia IPv6 para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Usando o utilitário Checkv4.exe aplicativo](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Apêndice A: Código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Apêndice B: Código-fonte Agnostic da versão IP](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



