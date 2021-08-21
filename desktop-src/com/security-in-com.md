---
title: Segurança em COM
description: A segurança em COM baseia-se firmemente na segurança fornecida pelo Windows e nos mecanismos de segurança RPC subjacentes.
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b197a632494545e5a151110ca17f1cf1ae1df7577a897284d1e5d437b74093f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918117"
---
# <a name="security-in-com"></a>Segurança em COM

A segurança em COM baseia-se firmemente na segurança fornecida pelo Windows e nos mecanismos de segurança RPC subjacentes. A segurança COM depende da autenticação *(o* processo de verificação da identidade de um chamador) e da autorização *(o* processo de determinar se um chamador está autorizado a fazer o que está solicitando). Há dois tipos principais de segurança no COM: segurança de *ativação e* *segurança de chamada.* A segurança de ativação determina se um cliente pode iniciar um servidor. Depois que um servidor tiver sido lançado, você poderá usar a segurança de chamada para controlar o acesso aos objetos de um servidor.

Nesse modelo de segurança, os servidores gerenciam e ajudam a proteger objetos, os clientes têm acesso a objetos por meio de servidores e os servidores podem tentar acessar ao representar o cliente.

O sistema implementa o protocolo de autenticação Kerberos v5 e o pacote de segurança Schannel. Ele também inclui recursos como representação de nível delegado, autenticação mútua, a capacidade de definir níveis de autenticação para uma AppID no Registro e a desaprodução. Usando a segurança COM, você pode implementar objetos que podem executar operações privilegiadas sem comprometer a segurança.

Como há uma ampla variedade de recursos de segurança COM disponíveis, é útil determinar inicialmente de que tipo de segurança seu aplicativo precisa. Para a maioria dos aplicativos, definir um nível aceitável de segurança pode ser um processo indolor, mas você também pode usar a segurança COM para dar suporte a cenários de segurança muito complexos.

Você pode definir o processo de segurança em todo o país, usando Dcomcnfg.exe para definir o registro ou chamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Duas interfaces principais, [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (e funções auxiliares associadas), permitem definir a segurança em nível de chamada em seu programa.

Para saber mais sobre a segurança COM, consulte os seguintes tópicos:

-   [Determinando suas necessidades de segurança](determining-your-security-needs.md)
-   [Padrões de segurança COM](com-security-defaults.md)
-   [Segurança de ativação](activation-security.md)
-   [Valores de segurança](security-values.md)
-   [Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
-   [Habilitando a segurança COM usando DCOMCNFG](enabling-com-security-using-dcomcnfg.md)
-   [Como desligar a segurança](turning-off-security.md)
-   [Segurança do lado do servidor](server-side-security.md)
-   [Negociação de garantia de segurança](security-blanket-negotiation.md)
-   [Pacotes COM e de segurança](com-and-security-packages.md)
-   [Aprimoramentos de segurança do DCOM no Windows XP Service Pack 2 e Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [Listas de controle de acesso para COM](access-control-lists-for-com.md)
-   [O Moniker de Elevação COM](the-com-elevation-moniker.md)

 

 