---
title: Active Directory Service Interfaces
description: Introdução às interfaces de serviços Active Directory, com links para guias diferentes.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Interfaces de serviço Active Directory (consulte ADSI)
- ADSI ADSI, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008363"
---
# <a name="active-directory-service-interfaces"></a>Active Directory Service Interfaces

## <a name="purpose"></a>Finalidade

A ADSI (Active Directory Service Interfaces) é um conjunto de interfaces COM usadas para acessar os recursos dos serviços de diretório de diferentes provedores de rede. A ADSI é usada em um ambiente de computação distribuído para apresentar um único conjunto de interfaces de serviço de diretório para gerenciar recursos de rede. Os administradores e desenvolvedores podem usar os serviços ADSI para enumerar e gerenciar os recursos em um serviço de diretório, não importa qual ambiente de rede contém o recurso.

A ADSI permite tarefas administrativas comuns, como a adição de novos usuários, o gerenciamento de impressoras e a localização de recursos em um ambiente de computação distribuído.

> [!Note]  
> A documentação a seguir destina-se a programadores de computadores. Se você for um usuário final tentando depurar um erro de impressão ou um problema de rede doméstica, consulte os [fóruns da Comunidade da Microsoft](https://answers.microsoft.com).

 

## <a name="where-applicable"></a>Quando aplicável

Os administradores de rede podem usar o ADSI para automatizar tarefas comuns, como adicionar usuários e grupos, gerenciar impressoras e definir permissões em recursos de rede.

Fornecedores independentes de software e desenvolvedores de usuários finais podem usar o ADSI para "diretório habilitado" para seus produtos e aplicativos. Os serviços podem se publicar em um diretório, os clientes podem usar o diretório para localizar os serviços, e ambos podem usar o diretório para localizar e manipular outros objetos de interesse. Como as interfaces de serviço do Active Directory são independentes dos serviços de diretório subjacentes, os produtos e aplicativos habilitados para diretório podem operar com êxito em vários ambientes de rede e de diretório.

## <a name="developer-audience"></a>Público de desenvolvedores

Você pode escrever aplicativos cliente ADSI em vários idiomas. Para a maioria das tarefas administrativas, a ADSI define interfaces e objetos acessíveis a partir de linguagens em conformidade com a automação, como o Microsoft Visual Basic, o Microsoft Visual Basic Scripting Edition (VBScript) e o Java, para obter mais linguagens de desempenho e eficiência, como C e C++. Uma boa base na programação COM é útil para o programador ADSI.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O Active Directory é executado em controladores de domínio do Windows Server. No entanto, os aplicativos cliente que usam ADSI podem ser escritos e executados no Windows. Além disso, os desenvolvedores deverão ter o SDK (Software Development Kit) da plataforma, também disponível no site do MSDN. Para investigar o conteúdo de Active Directory, use o snap-in do MMC usuários e computadores Active Directory. Esse snap-in substitui a ferramenta ADSVW que estava disponível para versões anteriores do Windows.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Sobre o ADSI](about-adsi.md)
</dt> <dd>

Informações gerais sobre ADSI.

</dd> <dt>

[Usando ADSI](using-adsi.md)
</dt> <dd>

Guia do programador para usar o ADSI.

</dd> <dt>

[Tutoriais de início rápido do ADSI](adsi-quick-start-tutorials.md)
</dt> <dd>

Usando o ADSI com a automação para gerenciar diretórios.

</dd> <dt>

[Referência ADSI](adsi-reference.md)
</dt> <dd>

Documentação de interfaces e métodos ADSI.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O Component Object Model](../com/the-component-object-model.md)
</dt> <dt>

[Clientes e servidores COM](../com/com-clients-and-servers.md)
</dt> <dt>

[Active Directory Domain Services](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 