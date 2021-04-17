---
description: Veja a seguir uma descrição de como criar um pacote de Windows Installer para instalar um assembly Win32.
ms.assetid: 1234e904-fc7f-4eb7-8c50-0c959bbf5261
title: Instalando assemblies do Win32 para compartilhamento lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea72c9bcb7bd85ac38dfc8857030d6b9d6afbf23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782792"
---
# <a name="installing-win32-assemblies-for-side-by-side-sharing"></a>Instalando assemblies do Win32 para compartilhamento lado a lado

Veja a seguir uma descrição de como criar um pacote de Windows Installer para instalar um assembly Win32. O pacote instala um assembly lado a lado na pasta WinSxS para o uso compartilhado do aplicativo. Depois de instalar o pacote, o assembly compartilhado está globalmente disponível para qualquer aplicativo que especifique uma dependência no assembly em um arquivo de manifesto do assembly. O instalador não registra globalmente o assembly lado a lado no sistema.

Observe que você pode instalar assemblies compartilhados lado a lado usando módulos de [mesclagem](merge-modules.md).

Antes de continuar, você deve entender como criar um pacote de Windows Installer sem assemblies. Para obter um exemplo de como criar uma instalação simples, consulte [um exemplo de instalação](an-installation-example.md).

**Para instalar um assembly compartilhado lado a lado**

1.  Defina um componente de Windows Installer que inclui o assembly Win32. Esse componente pode conter outros recursos que devem ser sempre instalados ou removidos com o assembly. Todos os outros componentes do aplicativo podem ser criados exatamente como para uma instalação sem assemblies. Adicione uma linha à [tabela de componentes](component-table.md) para o componente que contém o assembly Win32. Insira um [GUID](guid.md) de Windows Installer válido para este código de componente. Não use o arquivo de manifesto como o caminho de chave para este componente.
2.  Adicione uma linha à [tabela FeatureComponents](featurecomponents-table.md) vinculando o componente a um recurso Windows Installer. Para obter informações, consulte [componentes e recursos](components-and-features.md). Um recurso de Windows Installer deve ser uma parte da funcionalidade do aplicativo que pode ser reconhecível para um usuário. O assembly é ativado quando esse recurso é selecionado por um usuário ou com falha no por um aplicativo. Se o assembly definir um recurso adicional, adicione uma linha adicional à tabela de [recursos](feature-table.md) para os atributos do recurso. Esta etapa não é necessária ao criar um módulo de mesclagem.
3.  Para assemblies lado a lado, as informações de associação e de ativação, como classes COM, interfaces e bibliotecas de tipos, são armazenadas em arquivos de manifesto em vez de no registro. Os assemblies compartilhados armazenam essas informações em um manifesto do assembly. Em sistemas que dão suporte a assemblies lado a lado, o instalador ignora o processamento de qualquer informação sobre o componente inserido na [tabela de extensão](extension-table.md), [tabela de verbo](verb-table.md), tabela de [TypeLib](typelib-table.md), tabela de [classes](class-table.md) [MIME](mime-table.md), tabela de classe, tabela de [ProgID](progid-table.md)e [tabela AppID](appid-table.md). As informações de associação e ativação podem ser inseridas nessas tabelas para uso por sistemas que não dão suporte ao compartilhamento de assembly lado a lado.
4.  A instalação lado a lado não registra globalmente o assembly, o instalador ignora o registro automático do componente se alguma informação de auto-registro tiver sido inserida na [tabela selfreg](selfreg-table.md). As informações de Autoregistro podem ser inseridas na tabela SelfReg para o registro automático do componente em sistemas que não dão suporte ao compartilhamento de assembly lado a lado.
5.  Adicione outras informações de registro, exclusivas de associação e ativação ou Autoregistro do componente, à tabela [do registro](registry-table.md), à [tabela RemoveRegistry](removeregistry-table.md)e à [tabela de ambiente](environment-table.md).
6.  Como esse é um assembly compartilhado, não gere um arquivo. local. Não inclua informações para este componente na [tabela IsolatedComponent](isolatedcomponent-table.md). O instalador ignora a tabela IsolatedComponent para esse componente em sistemas operacionais que dão suporte ao compartilhamento lado a lado. Adicione informações à tabela IsolatedComponent se desejar que o assembly seja privado em sistemas que dão suporte a arquivos. local.
7.  Para habilitar o compartilhamento lado a lado, o assembly do Win32 deve ser instalado na pasta WinSxS. Isso é feito deixando a \_ coluna de aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md) nula para o assembly. Isso informa o instalador para instalar o assembly na pasta WinSxS, em vez de na pasta do componente. Adicione uma linha à [tabela MsiAssembly](msiassembly-table.md) para o componente que contém o assembly Win32. Insira um valor de 1 no campo atributos da tabela MsiAssembly para especificar que este é um assembly Win32. Para um assembly compartilhado, deixe o \_ campo aplicativo de arquivo vazio. Adicione a [ação MsiPublishAssemblies](msipublishassemblies-action.md) à [tabela InstallExecuteSequence](installexecutesequence-table.md) ou à [tabela AdvtExecuteSequence](advtexecutesequence-table.md). Adicione a [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md) à tabela InstallExecuteSequence.
8.  Adicione linhas à [tabela MsiAssemblyName](msiassemblyname-table.md) para o componente. Adicione uma linha para cada par de nome e valor especificado na seção assemblyIdentity do manifesto. Para obter um exemplo, consulte [tabela MsiAssemblyName](msiassemblyname-table.md).

 

 



