---
title: Responsabilidades do servidor COM
description: Responsabilidades do servidor COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c6604a8f42804867e797087ffb346fe69152cb84440d052560c3f40a42140c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854766"
---
# <a name="com-server-responsibilities"></a>Responsabilidades do servidor COM

Uma das maneiras mais importantes para um cliente obter um ponteiro para um objeto é solicitar que um servidor seja lançado e que uma instância do objeto fornecida pelo servidor seja criada e ativada. É responsabilidade do servidor garantir que isso ocorra corretamente. Há várias partes importantes para isso.

O servidor deve implementar o código para um objeto de classe por meio de uma implementação da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2.**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)

O servidor deve registrar seu CLSID no registro do sistema no computador no qual ele reside e, além disso, tem a opção de publicar seu local do computador em outros sistemas em uma rede para permitir que os clientes o chamem sem exigir que o cliente saiba o local do servidor.

O servidor é responsável principalmente pela segurança; ou seja, na maior parte do tempo, o servidor determina se ele fornecerá um ponteiro para um de seus objetos para um cliente.

Os servidores em processo devem implementar e exportar determinadas funções que permitem que o processo do cliente as insinue.

Os tópicos a seguir detalham as responsabilidades do servidor COM:

-   [Implementando IClassFactory](implementing-iclassfactory.md)
-   [Licensing e IClassFactory2](licensing-and-iclassfactory2.md)
-   [Registrando servidores COM](registering-com-servers.md)
-   [Auxiliares de implementação de servidor fora de processo](out-of-process-server-implementation-helpers.md)
-   [Criação e otimizações de GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 