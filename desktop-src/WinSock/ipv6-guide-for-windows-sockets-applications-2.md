---
description: Este guia fornece as informações necessárias para permitir que seu aplicativo do Microsoft Windows Use a próxima geração de protocolo de Internet, versão 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guia IPv6 para aplicativos do Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090381"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>Guia IPv6 para aplicativos do Windows Sockets

Este guia fornece as informações necessárias para permitir que seu aplicativo do Microsoft Windows Use a próxima geração de protocolo de Internet, versão 6 (IPv6). A adição do recurso IPv6 ao seu aplicativo não é necessariamente um processo de portabilidade. Para portar um aplicativo sugere a modificação do código para funcionar em uma plataforma diferente, o que implica deixar a plataforma anterior por trás. Este guia é especificamente estruturado para ajudar a adicionar funcionalidades IPv6 a um aplicativo e, ao mesmo tempo, manter a funcionalidade IPv4.

Este guia aborda os problemas associados à adição da funcionalidade IPv6 e, em seguida, direciona as áreas de desenvolvimento mais afetadas pela transição. Cada área recebe uma explicação completa das armadilhas a serem observadas, as estratégias sugeridas para evitá-las e dicas sobre como fazer o melhor uso de novos elementos programáticos do [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funções e estruturas). Para obter informações adicionais sobre o IPv6, consulte [suporte a IPv6](ipv6-support-2.md).

Este guia também fornece exemplos de código para dar a você experiência prática e representações visuais dos problemas que você pode encontrar ao modificar seus aplicativos. Os exemplos vêm de exemplos completos e funcionais de um aplicativo simples do Windows Sockets que foi modificado para dar suporte a IPv4 e IPv6. O código-fonte para esses exemplos de trabalho está incluído em sua totalidade em dois apêndices no final deste documento: [Apêndice A: o código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md) inclui o código-fonte de um aplicativo antes que ele seja modificado para dar suporte a IPv6; [Apêndice B: o código-fonte independente da versão IP](appendix-b-ip-version-agnostic-source-code-2.md) fornece o código-fonte após o aplicativo ter sido habilitado para IPv6.

A Microsoft fornece um utilitário chamado Checkv4.exe que ajuda você a encontrar código potencialmente sensível à portabilidade no código do aplicativo e também faz recomendações para correções. O utilitário Checkv4.exe é demonstrado neste documento, usando o aplicativo de exemplo incluído nos apêndices, juntamente com capturas de tela que exibem a saída que o utilitário Checkv4.exe produz. Para obter mais informações, consulte [usando o utilitário Checkv4.exe](using-the-checkv4-exe-utility-2.md).

As áreas de programação abordadas por este guia são:

-   [Alterando estruturas de dados para aplicativos Winsock do IPv6](changing-data-structures-2.md)
-   [Chamadas de função para aplicativos Winsock IPv6](function-calls-2.md)
-   [Uso de endereços IPv4 codificados](use-of-hardcoded-ipv4-addresses-2.md)
-   [Problemas de interface do usuário para aplicativos Winsock do IPv6](user-interface-issues-2.md)
-   [Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
-   [Soquetes de pilha dupla para aplicativos Winsock do IPv6](dual-stack-sockets.md)

Como não há nenhuma sequência uniforme de eventos, as seções que resolvem problemas de habilitação de IPv6 não são organizadas de maneira sequencialmente significativa, para que você possa fazer referência a qualquer seção a qualquer momento. É altamente recomendável que você examine cada seção enquanto adiciona a funcionalidade IPv6 ao seu aplicativo. Também é aconselhável ler sobre o utilitário Checkv4.exe, pois ele inclui dicas sobre a ordem em que os problemas de habilitação do IPv6 são abordados.

Para examinar o utilitário Checkv4.exe e examinar a ordem na qual você deve abordar o processo de portabilidade em seus aplicativos, consulte [usando o utilitário Checkv4.exe](using-the-checkv4-exe-utility-2.md). Esta seção inclui informações sobre um sinalizador de tempo de compilação que verifica estritamente os elementos de programação incompatíveis com o IPv6.

Para ir direto para o aplicativo de exemplo, consulte [o apêndice a: código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md) e [Apêndice B: código-fonte independente da versão IP](appendix-b-ip-version-agnostic-source-code-2.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protocolo IP versão 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Suporte a IPv6](ipv6-support-2.md)
</dt> <dt>

[Versão prévia da tecnologia IPv6 para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Usando o utilitário Checkv4.exe](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Apêndice A: código-fonte somente IPv4](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Apêndice B: código-fonte independente da versão IP](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



