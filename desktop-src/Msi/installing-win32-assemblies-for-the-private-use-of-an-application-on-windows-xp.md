---
description: O procedimento neste tópico identifica como criar um pacote de Windows Installer para instalar um assembly Win32.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: Instalando assemblies do Win32 para o uso particular de um aplicativo no Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e807e22c9c5dea67ece5ead0ded95f06ab203689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812919"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>Instalando assemblies do Win32 para o uso particular de um aplicativo no Windows XP

O procedimento neste tópico identifica como criar um pacote de Windows Installer para instalar um assembly Win32. O pacote instala o assembly e um arquivo de manifesto do aplicativo em uma pasta criada que o aplicativo usa. O manifesto do aplicativo especifica a dependência do aplicativo no assembly particular. Depois de instalar o pacote, o assembly privado estará disponível para uso exclusivo do aplicativo. A dependência do assembly que é especificada no manifesto do aplicativo substitui (para este aplicativo) quaisquer outras dependências de assembly globais especificadas nos arquivos de manifesto do assembly.

Antes de continuar, é uma boa ideia entender como criar um pacote de Windows Installer sem assemblies. Para obter mais informações, consulte [um exemplo de instalação](an-installation-example.md).

**Para instalar um assembly particular no Windows XP**

1.  Defina um componente de Windows Installer que inclui o assembly Win32 e o arquivo de manifesto do aplicativo. Esse componente pode conter outros recursos que devem ser sempre instalados ou removidos com o assembly. As etapas restantes deste procedimento descrevem como criar o banco de dados de instalação para instalar esse componente.
2.  Adicione uma linha à [tabela de componentes](component-table.md) para o componente que contém o assembly do Win32 e o arquivo de manifesto do aplicativo. Insira um [GUID](guid.md) de Windows Installer válido para este código de componente. Para obter mais informações, consulte [alterando o código do componente](changing-the-component-code.md) e [o que acontece se as regras de componente forem interrompidas?](what-happens-if-the-component-rules-are-broken.md)
3.  O instalador copia o arquivo de manifesto do assembly na pasta que contém o arquivo especificado no \_ campo aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md).
4.  Adicione uma linha à [tabela FeatureComponents](featurecomponents-table.md) vinculando o componente a um recurso Windows Installer. Para obter mais informações, consulte [componentes e recursos](components-and-features.md). Um recurso de Windows Installer deve ser uma parte da funcionalidade do aplicativo que um usuário pode reconhecer. O assembly é ativado quando esse recurso é selecionado por um usuário ou com falha no por um aplicativo. Se o assembly definir um recurso adicional, adicione uma linha adicional à tabela de [recursos](feature-table.md) para os atributos de recurso. Esta etapa não será necessária se você criar um módulo de mesclagem.
5.  Para assemblies lado a lado, as informações de associação e de ativação, por exemplo, classes COM, interfaces e bibliotecas de tipos, são armazenadas em arquivos de manifesto em vez de no registro. Os assemblies privados armazenam essas informações em um manifesto do assembly. Em sistemas que dão suporte a assemblies lado a lado, o instalador ignora o processamento de qualquer informação sobre o componente que é inserido na [tabela de extensão](extension-table.md), [tabela de verbo](verb-table.md), tabela de [TypeLib](typelib-table.md), tabela [MIME](mime-table.md), tabela de [classes](class-table.md), tabela [ProgID](progid-table.md)e [tabela AppID](appid-table.md). As informações de associação e ativação podem ser inseridas nas tabelas para uso por sistemas que não dão suporte ao compartilhamento de assembly lado a lado.
6.  A instalação lado a lado não registra o assembly globalmente. O instalador ignora o registro automático do componente se alguma informação de auto-registro for inserida na [tabela selfreg](selfreg-table.md). As informações de Autoregistro podem ser inseridas na tabela SelfReg para o registro automático do componente em sistemas que não dão suporte ao compartilhamento de assembly lado a lado.
7.  Adicione outras informações de registro, exclusivas de associação e ativação ou Autoregistro do componente, à tabela [do registro](registry-table.md), à [tabela RemoveRegistry](removeregistry-table.md)e à [tabela de ambiente](environment-table.md).
8.  O instalador ignora a [tabela IsolatedComponent](isolatedcomponent-table.md) para esse componente em sistemas operacionais que dão suporte ao compartilhamento lado a lado. Insira as informações nesta tabela se você quiser que o assembly seja privado em sistemas que dão suporte a arquivos locais.
9.  Adicione uma linha à [tabela MsiAssembly](msiassembly-table.md) para o componente que contém o assembly Win32. Insira um valor de 1 no campo atributos da tabela MsiAssembly para especificar que este é um assembly Win32. Insira a chave de arquivo do assembly privado no \_ campo aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md). Adicione a [ação MsiPublishAssemblies](msipublishassemblies-action.md) à [tabela InstallExecuteSequence](installexecutesequence-table.md) ou à [tabela AdvtExecuteSequence](advtexecutesequence-table.md). Adicione a [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md) à tabela InstallExecuteSequence. Crie uma pasta para o assembly e o arquivo de manifesto na [tabela de diretórios](directory-table.md). Essa pasta deve estar no diretório raiz do aplicativo e conter o arquivo especificado no \_ campo aplicativo de arquivo da [tabela MsiAssembly](msiassembly-table.md). Durante a instalação do aplicativo, o instalador resolve a [tabela de diretórios](directory-table.md) para o caminho para essa pasta. Para obter mais informações, consulte [usando a tabela de diretórios](using-the-directory-table.md).
10. Adicione linhas à [tabela MsiAssemblyName](msiassemblyname-table.md) para o componente. Adicione uma linha para cada par de nome e valor especificado na seção assemblyIdentity do manifesto. Para obter mais informações, consulte [tabela MsiAssemblyName](msiassemblyname-table.md).

 

 



