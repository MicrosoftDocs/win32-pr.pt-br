---
title: Responsabilidades do servidor COM
description: Responsabilidades do servidor COM
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366761"
---
# <a name="com-server-responsibilities"></a>Responsabilidades do servidor COM

Uma das maneiras mais importantes para um cliente obter um ponteiro para um objeto é o cliente solicitar que um servidor seja iniciado e que uma instância do objeto fornecida pelo servidor seja criada e ativada. É responsabilidade do servidor garantir que isso aconteça corretamente. Há várias partes importantes para isso.

O servidor deve implementar o código para um objeto de classe por meio de uma implementação da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) .

O servidor deve registrar seu CLSID no registro do sistema no computador em que ele reside e ainda mais, tem a opção de publicar seu local de computador em outros sistemas em uma rede para permitir que os clientes o chamem sem exigir que o cliente saiba o local do servidor.

O servidor é responsável principalmente pela segurança; ou seja, para a maior parte, o servidor determina se ele fornecerá um ponteiro para um de seus objetos a um cliente.

Os servidores em processo devem implementar e exportar determinadas funções que permitam ao processo do cliente instanciá-las.

Os tópicos a seguir detalham as responsabilidades do servidor COM:

-   [Implementando IClassFactory](implementing-iclassfactory.md)
-   [Licenciamento e IClassFactory2](licensing-and-iclassfactory2.md)
-   [Registrando servidores COM](registering-com-servers.md)
-   [Auxiliares de implementação do servidor fora do processo](out-of-process-server-implementation-helpers.md)
-   [Criação e otimizações de GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 