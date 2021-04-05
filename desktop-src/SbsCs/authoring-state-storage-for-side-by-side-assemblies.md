---
description: Ao criar seus próprios assemblies lado a lado, siga as diretrizes para criar assemblies lado a lado e criar qualquer DLL a ser incluída no assembly de acordo com as diretrizes de criação de uma DLL para um assembly lado a lado.
ms.assetid: 0e98bbcd-7e23-4a33-b0fa-1f936d0ef96b
title: Criação de armazenamento de estado para assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee388cf680ee3a186a225ca7e3bde8b6eae625d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662425"
---
# <a name="authoring-state-storage-for-side-by-side-assemblies"></a>Criação de armazenamento de estado para assemblies lado a lado

Ao criar seus próprios assemblies lado a lado, siga as [diretrizes para criar assemblies](guidelines-for-creating-side-by-side-assemblies.md) lado a lado e criar qualquer DLL a ser incluída no assembly de acordo com as diretrizes de [criação de uma dll para um assembly lado a lado](authoring-a-dll-for-a-side-by-side-assembly.md).

Siga as seguintes diretrizes para o armazenamento do Estado:

-   O armazenamento de estado de design para ser compatível com versões posteriores e retroativas. Espere que as versões sejam usadas em qualquer ordem: por exemplo, v1, depois v3 e v2.
-   Inicialize e defina as configurações padrão para o assembly no código do assembly. Não salve as configurações de padrões no registro.
-   As configurações do registro devem ser gravadas em uma base de versão individual para isolar várias versões de assembly que podem ser executadas ao mesmo tempo. Projete seu assembly lado a lado para armazenar corretamente e manipular o estado do assembly durante cenários de compartilhamento lado a lado.
-   Assemblies normalmente armazenam informações de estado em chaves do registro. Crie um conjunto de arquivos de cabeçalho e funções auxiliares para fornecer uma maneira fácil para as chaves de registro de versão que contêm o estado do assembly.
-   Todas as informações de estado do assembly salvas no registro devem ser isoladas de outras versões do assembly. As configurações de estado armazenadas no registro devem ser salvas em seções de versão individuais do registro. Isso é necessário nas partes HKLM e HKCU do registro. Por exemplo, armazene configurações de estado HKCU para o assembly versão XXXX na seguinte chave do registro:

    **HKCU** \\ **MyCompany** \\ **MyComponent** \\ **VersionXXXX**

-   Todas as informações de estado armazenadas no registro por assemblies compartilhados devem ser salvas em seções de versão individuais do registro. Por exemplo, uma configuração de estado chamada EnableSuperCoolFeature pode ter um valor de **true** ou **false**. Armazene o valor de um [*assembly compartilhado lado a lado*](s-sbscs-gly.md) da seguinte maneira:

    **HKEY \_ CurrentUser** \\ **software** \\ **MyCompany** \\ **myComponent** \\ **versão 01.01** \\ **EnableSuperCoolFeature = true**

-   Todas as informações de estado armazenadas no registro por assemblies privados devem ser salvas em seções de aplicativo individuais do registro. Isso isola as configurações de estado do assembly para o aplicativo. Você pode usar a função [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) para configurar uma raiz virtual. Por exemplo, se a versão do assembly XXYY for um assembly particular de "SomeApplication", uma chamada para **GetModuleFileName** retornará "SomeApplication" e quaisquer configurações de estado privado para o assembly deverão ser gravadas na seguinte chave:

    **HKCU** \\ **MyCompany** \\ **MyComponent** \\ **VersionXXYY** \\ **SomeApplication**

-   Faça as configurações de estado compartilhado armazenadas no registro privado para o contexto do assembly que executa o. Você pode usar a função [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) para configurar uma raiz virtual. Isso deve ser feito para as ramificações HKLM e HKCU.
-   O ideal é que você adote um modelo de persistência no qual o aplicativo persiste o estado e não altera o registro. Um aplicativo não deve precisar tocar diretamente nas entradas do registro do componente. Em vez disso, o assembly deve oferecer funções de API que salvam ou restauram configurações que são compatíveis.
-   Os assemblies podem salvar as configurações de estado em lojas fora do registro para permitir que o assembly interaja com o estado global. Os assemblies lado a lado podem usar os seguintes repositórios compatíveis:
    -   Um repositório protegido (*Pstore*)
    -   Um cache do WinInet
    -   Um Microsoft SQL Server

 

 
