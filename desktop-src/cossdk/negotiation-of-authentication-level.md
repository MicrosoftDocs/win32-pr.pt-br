---
description: Negociação de nível de autenticação
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Negociação de nível de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784504"
---
# <a name="negotiation-of-authentication-level"></a>Negociação de nível de autenticação

Tanto o cliente quanto o servidor devem participar da autenticação, e cada parte indica que ele deseja executar um determinado nível de autenticação. No início de uma chamada, o nível de autenticação é negociado entre as duas partes, um serviço apropriado é escolhido e a chamada é autenticada e prossegue (com possível criptografia, dependendo do nível de autenticação escolhido). O nível de autenticação negociado entre o cliente e o servidor é determinado como máximo (*preferência do cliente*, *preferência do servidor*). O efeito disso significa que o servidor sempre pode determinar um nível mínimo de autenticação com o qual ele se sente confortável; ou seja, a autenticação pode ser ditada administrativamente do servidor.

O cliente especifica que deseja executar a autenticação em um determinado nível como com qualquer aplicativo COM. O nível de autenticação do cliente pode ser indicado da seguinte maneira:

-   Por computador cliente, com o nível de autenticação COM de todo o computador definido usando [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) ou a ferramenta administrativa serviços de componentes.
-   Por aplicativo cliente administrativamente, usando [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) ou usando a ferramenta administrativa serviços de componentes se o cliente deve ser um aplicativo com+.
-   Por processo de cliente de forma programática, com [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   A qualquer momento programaticamente, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

O aplicativo do servidor COM+ especifica um nível de autenticação administrativamente usando a ferramenta administrativa serviços de componentes (ou por meio de um script administrativo).

A negociação de autenticação para uma chamada continua na seguinte sequência:

1.  O nível de autenticação é escolhido como máximo (*cliente*, *servidor*).
2.  Negociação do protocolo de autenticação.
3.  O servidor autentica a identidade do cliente.
4.  Opcionalmente, o cliente autentica a identidade do servidor, dependendo do protocolo de autenticação.
5.  As chamadas de método são comunicadas com o nível escolhido de autenticação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação de cliente](client-authentication.md)
</dt> </dl>

 

 
