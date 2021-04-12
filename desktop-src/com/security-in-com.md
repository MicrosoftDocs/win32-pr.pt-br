---
title: Segurança em COM
description: A segurança no COM é firmemente baseada na segurança fornecida pelo Windows e nos mecanismos de segurança RPC subjacentes.
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5e462317d85f7c445d4d8a5ae0aa4d9d3ee724
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366774"
---
# <a name="security-in-com"></a>Segurança em COM

A segurança no COM é firmemente baseada na segurança fornecida pelo Windows e nos mecanismos de segurança RPC subjacentes. A segurança COM conta COM a *autenticação* (o processo de verificar a identidade de um chamador) e a *autorização* (o processo de determinar se um chamador está autorizado a fazer o que está pedindo). Há dois tipos principais de segurança em COM: *segurança de ativação* e *chamada de segurança*. A segurança de ativação determina se um cliente pode iniciar um servidor. Depois que um servidor tiver sido iniciado, você poderá usar a segurança de chamada para controlar o acesso aos objetos de um servidor.

Nesse modelo de segurança, os servidores gerenciam e ajudam a proteger objetos, os clientes obtêm acesso a objetos por meio de servidores e os servidores podem tentar o acesso enquanto estão representando o cliente.

O sistema implementa o protocolo de autenticação Kerberos V5 e o pacote de segurança Schannel. Ele também inclui recursos como representação de nível delegado, autenticação mútua, a capacidade de definir níveis de autenticação para um AppID no registro e o encobrimento. Usando a segurança COM, você pode implementar objetos que podem executar operações privilegiadas sem comprometer a segurança.

Como há uma ampla variedade de recursos de segurança COM disponíveis, é útil determinar inicialmente o tipo de segurança de que seu aplicativo precisa. Para a maioria dos aplicativos, a definição de um nível aceitável de segurança pode ser um processo simples, mas você também pode usar a segurança COM para dar suporte a cenários de segurança muito complexos.

Você pode definir processwide de segurança usando Dcomcnfg.exe para definir o registro ou chamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Duas interfaces primárias, [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (e funções auxiliares associadas) permitem que você defina a segurança em nível de chamada em seu programa.

Para saber mais sobre a segurança COM, consulte os seguintes tópicos:

-   [Determinando suas necessidades de segurança](determining-your-security-needs.md)
-   [Padrões de segurança COM](com-security-defaults.md)
-   [Segurança de ativação](activation-security.md)
-   [Valores de segurança](security-values.md)
-   [Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
-   [Habilitando a segurança COM usando DCOMCNFG](enabling-com-security-using-dcomcnfg.md)
-   [Desativando a segurança](turning-off-security.md)
-   [Segurança no lado do servidor](server-side-security.md)
-   [Negociação em cobertura de segurança](security-blanket-negotiation.md)
-   [Pacotes de segurança e COM](com-and-security-packages.md)
-   [Aprimoramentos de segurança DCOM no Windows XP Service Pack 2 e no Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [Listas de controle de acesso para COM](access-control-lists-for-com.md)
-   [O moniker de elevação COM](the-com-elevation-moniker.md)

 

 