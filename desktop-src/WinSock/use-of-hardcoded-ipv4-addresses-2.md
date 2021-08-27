---
description: A longevidade de IPv4 resultou na codificação de muitos endereços IPv4 conhecidos, como endereços de loopback (127.x.x.x), constantes de inteiro, como LOOPBACK INADDR, entre \_ outros.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Uso de endereços IPv4 em código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0506f200776402464c4b2904435157c435ece7fc2c6d9e0b10bfd1c1d66491
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121196"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Uso de endereços IPv4 em código

A longevidade de IPv4 resultou na codificação de muitos endereços IPv4 conhecidos, como endereços de loopback (127.x.x.x), constantes de inteiro, como LOOPBACK INADDR, entre \_ outros. A prática de codificar esses endereços apresenta problemas óbvios ao modificar e ao aplicativo existente para dar suporte a IPv6 ou criar novos programas independentes de versão de IP.

Melhor prática

-   A melhor abordagem é evitar a hardcodin de quaisquer endereços.

Código a ser evitado

-   Evite usar endereços codificados no código.

**Para modificar sua base de código existente de IPv4 para interoperabilidade IPv4 e IPv6**

1.  Adquira *oCheckv4.exe* utilitário. O *Checkv4.exe* utilitário é instalado como parte do Microsoft Windows Software Development Kit (SDK) lançado para Windows Vista e posterior. O Windows SDK está disponível por meio de uma assinatura do MSDN e também pode ser baixado no site da Microsoft ( https://msdn.microsoft.com) .
2.  Execute o *utilitárioCheckv4.exe* em seu código. Saiba mais sobre como executar o *utilitárioCheckv4.exe* em seus arquivos na seção usando o utilitário [Checkv4.exe .](using-the-checkv4-exe-utility-2.md)
3.  O *Checkv4.exe* o alerta para a presença de definições comuns para endereços IPv4, como \_ LOOPBACK INADDR. Modifique qualquer código que use cadeias de caracteres literais com código que seja agnóstico de versão de protocolo.
4.  Pesquise sua base de código para outras cadeias de caracteres literais potenciais, conforme apropriado.

O *Checkv4.exe* utilitário pode ajudá-lo a encontrar cadeias de caracteres literais comuns, mas pode haver outras específicas para seu aplicativo. Você deve executar uma pesquisa e testes completos para garantir que sua base de código tenha eliminado possíveis problemas associados a cadeias de caracteres literais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia IPv6 para aplicativos Windows soquetes](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Alterando estruturas de dados para aplicativos Winsock IPv6](changing-data-structures-2.md)
</dt> <dt>

[Soquetes de pilha dupla para aplicativos Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chamadas de função para aplicativos Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Interface do Usuário problemas para aplicativos Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 



