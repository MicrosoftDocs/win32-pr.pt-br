---
title: Active Directory Domain Services
description: A Microsoft Active Directory Domain Services é a base para redes distribuídas criadas nos sistemas operacionais Windows 2000 Server, Windows Server 2003 e Microsoft Windows Server 2008 que usam controladores de domínio.
ms.assetid: 9fc78c72-c59c-4c4d-ace5-00a431645c4b
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory
- Active Directory Active Directory, página inicial
- Active Directory Domain Services Active Directory, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0270f331a68d23ad89a8e5a999f8cabd95487020
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008568"
---
# <a name="active-directory-domain-services"></a>Active Directory Domain Services

## <a name="purpose"></a>Finalidade

A Microsoft Active Directory Domain Services é a base para redes distribuídas criadas nos sistemas operacionais Windows 2000 Server, Windows Server 2003 e Microsoft Windows Server 2008 que usam controladores de domínio. Active Directory Domain Services fornecem armazenamento de dados hierárquicos seguro e estruturado para objetos em uma rede, como usuários, computadores, impressoras e serviços. Active Directory Domain Services fornecer suporte para localizar e trabalhar com esses objetos.

Este guia fornece uma visão geral do Active Directory Domain Services e do código de exemplo para tarefas básicas, como Pesquisar objetos e ler propriedades para tarefas mais avançadas, como publicação de serviço.

O Windows 2000 Server e os sistemas operacionais posteriores fornecem uma interface do usuário para que os usuários e administradores trabalhem com os objetos e dados no Active Directory Domain Services. Este guia descreve como estender e personalizar essa interface do usuário. Ele também descreve como estender Active Directory Domain Services definindo novas classes de objeto e atributos.

> [!Note]  
> A documentação a seguir destina-se a programadores de computadores. Se você for um usuário final tentando depurar um erro de impressão ou um problema de rede doméstica, consulte os [fóruns da Comunidade da Microsoft](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Quando aplicável

Os administradores de rede gravam scripts e aplicativos que acessam Active Directory Domain Services para automatizar tarefas administrativas comuns, como adicionar usuários e grupos, gerenciar impressoras e definir permissões para recursos de rede.

Fornecedores independentes de software e desenvolvedores de usuário final podem usar Active Directory Domain Services programação para habilitar o diretório de seus produtos e aplicativos. Os serviços podem se publicar em Active Directory Domain Services; Os clientes podem usar Active Directory Domain Services para localizar serviços, e ambos podem usar Active Directory Domain Services para localizar e trabalhar com outros objetos em uma rede.

## <a name="developer-audience"></a>Público de desenvolvedores

Os aplicativos que acessam dados no Active Directory Domain Services podem ser gravados usando a API de [interfaces de serviço do Active Directory](../adsi/active-directory-service-interfaces-adsi.md) , a API do protocolo de acesso ao [diretório leve](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) ou o namespace [System. DirectoryServices](/dotnet/api/system.directoryservices) .

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

Active Directory Domain Services executado no Windows 2000 e em controladores de domínio posteriores. No entanto, os aplicativos cliente podem ser escritos e executados no Windows Vista, no Windows Server 2003, no Windows XP, no Windows 2000, no Windows NT 4,0, no Windows 98 e no Windows 95.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Sobre Active Directory Domain Services](about-active-directory-domain-services.md)
</dt> <dd>

Informações gerais sobre Active Directory Domain Services.

</dd> <dt>

[Usar o Active Directory Domain Services](using-active-directory-domain-services.md)
</dt> <dd>

Guia de programação do Active Directory Domain Services.

</dd> <dt>

[Referência de Active Directory Domain Services](active-directory-domain-services-reference.md)
</dt> <dd>

Active Directory Domain Services referência de programação.

</dd> </dl>

 

 