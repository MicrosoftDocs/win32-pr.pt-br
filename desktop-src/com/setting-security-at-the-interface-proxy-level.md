---
title: Definindo a segurança no nível de proxy da interface
description: Às vezes, o cliente precisa de um controle refinado sobre a segurança em chamadas para interfaces específicas.
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b38fe83e8ce8841cc9029808a6947ec67d4eaf4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105814138"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>Definindo a segurança no nível de proxy da interface

Às vezes, o cliente precisa de um controle refinado sobre a segurança em chamadas para interfaces específicas. Por exemplo, a segurança pode ser definida em um nível baixo para o processo, mas as chamadas para uma interface específica podem exigir um nível de autenticação mais alto, como criptografia. Os métodos da interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) permitem que o cliente altere as configurações de segurança associadas a chamadas para uma interface específica controlando as configurações de segurança no nível de proxy de interface.

O cliente pode consultar um objeto existente para [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e, em seguida, chamar o método [**IClientSecurity:: QueryBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) para descobrir quais são as configurações de segurança atuais para um determinado proxy de interface. O método [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) pode ser usado para modificar as configurações de segurança de um proxy de interface individual no objeto antes de chamar um dos métodos da interface. As novas configurações se aplicam a quaisquer chamadores futuros dessa interface específica. O método [**IClientSecurity:: CopyProxy**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy) fornece uma maneira para o cliente copiar um proxy de interface para que as chamadas subsequentes para **setampla** na cópia não afetem os chamadores do proxy original.

O seteleve [**normalmente é usado**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) para aumentar o nível de autenticação de um determinado proxy de interface para um nível mais alto de proteção de segurança. No entanto, em algumas situações, também pode ser útil reduzir o nível de autenticação para um determinado proxy de interface. Por exemplo, suponha que o nível de autenticação padrão para o processo seja um valor diferente do RPC \_ C \_ Authn \_ nível \_ None e o cliente e o servidor estejam em domínios separados que não confiam uns nos outros. Nesse caso, as chamadas para o servidor falharão, a menos que o cliente chame para reduzir o **nível de autenticação** para RPC \_ C \_ Authn \_ nível \_ None.

Os clientes que usam a implementação padrão de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) fornecidos pelo Gerenciador de proxy podem chamar as funções auxiliares [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)e [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) em vez de chamar os métodos **IClientSecurity** diretamente. As funções auxiliares simplificam o código, mas são um pouco menos eficientes do que chamar os métodos **IClientSecurity** correspondentes diretamente.

A interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) é implementada localmente para o cliente pelo Gerenciador de proxy. Alguns objetos empacotados personalizados podem não dar suporte a **IClientSecurity**.

O [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) funciona com todos os serviços de autenticação com suporte (atualmente, NTLMSSP, Schannel e o protocolo Kerberos V5).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 