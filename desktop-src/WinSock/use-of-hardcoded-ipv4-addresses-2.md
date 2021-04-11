---
description: A longevidade do IPv4 resultou em codificação rígida de muitos endereços IPv4 conhecidos, como endereços de loopback (127. x. x. x), constantes de inteiros como, por exemplo \_ , loopback de inaddr, entre outros.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Uso de endereços IPv4 codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296340"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Uso de endereços IPv4 codificados

A longevidade do IPv4 resultou em codificação rígida de muitos endereços IPv4 conhecidos, como endereços de loopback (127. x. x. x), constantes de inteiros como, por exemplo \_ , loopback de inaddr, entre outros. A prática de codificação rígida desses endereços apresenta problemas óbvios durante a modificação e o aplicativo existente para dar suporte ao IPv6 ou à criação de novos programas independentes de versão de IP.

Melhor prática

-   A melhor abordagem é evitar o código de codificação de endereços.

Código a ser evitado

-   Evite usar endereços codificados no código.

**Para modificar sua base de código existente de IPv4 para IPv4 e IPv6-interoperabilidade**

1.  Adquira o utilitário *Checkv4.exe* . O utilitário *Checkv4.exe* é instalado como parte do SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior. O SDK do Windows está disponível por meio de uma assinatura do MSDN e também pode ser baixado do site da Microsoft ( https://msdn.microsoft.com) .
2.  Execute o utilitário *Checkv4.exe* em relação ao seu código. Saiba mais sobre como executar o utilitário de *Checkv4.exe* em seus arquivos na seção sobre como [usar o utilitário de Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  O utilitário *Checkv4.exe* alerta você sobre a presença de definições comuns para endereços IPv4, como inaddr \_ loopback. Modifique qualquer código que use cadeias de caracteres literais com código que seja independente de versão de protocolo.
4.  Pesquise sua base de código para outras possíveis cadeias de caracteres literais, conforme apropriado.

O utilitário *Checkv4.exe* pode ajudá-lo a encontrar cadeias de caracteres literais comuns, mas pode haver outros que são específicas do seu aplicativo. Você deve executar a pesquisa e os testes completos para garantir que sua base de código tenha potencialmente possíveis problemas associados a cadeias de caracteres literais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia IPv6 para aplicativos do Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Alterando estruturas de dados para aplicativos Winsock do IPv6](changing-data-structures-2.md)
</dt> <dt>

[Soquetes de pilha dupla para aplicativos Winsock do IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chamadas de função para aplicativos Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Problemas de interface do usuário para aplicativos Winsock do IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 



