---
description: O procedimento neste tópico identifica como criar um pacote Windows Instalador para instalar um assembly Win32.
ms.assetid: 2d4bc2be-cce6-45e6-b6a7-7ff96d28eb96
title: Instalando assemblies Win32 para o uso privado de um aplicativo no Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f478bddeb04ca9112610bd88338437002082204cc62078bde200539a8a18b6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893806"
---
# <a name="installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp"></a>Instalando assemblies Win32 para o uso privado de um aplicativo no Windows XP

O procedimento neste tópico identifica como criar um pacote Windows Instalador para instalar um assembly Win32. O pacote instala o assembly e um arquivo de manifesto do aplicativo em uma pasta de autor que o aplicativo usa. O manifesto do aplicativo especifica a dependência do aplicativo no assembly privado. Depois de instalar o pacote, o assembly privado estará disponível para uso exclusivo do aplicativo. A dependência de assembly especificada no manifesto do aplicativo substitui (para este aplicativo) quaisquer outras dependências de assembly globais especificadas nos arquivos de manifesto do assembly.

Antes de continuar, é uma boa ideia entender como Windows pacote do instalador sem assemblies. Para obter mais informações, consulte [Um exemplo de instalação](an-installation-example.md).

**Para instalar um assembly privado no Windows XP**

1.  Defina um Windows instalador que inclui o assembly Win32 e o arquivo de manifesto do aplicativo. Esse componente pode conter outros recursos que sempre devem ser instalados ou removidos com o assembly. As etapas restantes deste procedimento descrevem como autor do banco de dados de instalação para instalar esse componente.
2.  Adicione uma linha à tabela [Componente para](component-table.md) o componente que contém o assembly Win32 e o arquivo de manifesto do aplicativo. Insira um GUID Windows [instalador válido](guid.md) para este código de componente. Para obter mais informações, consulte [Alterando o código do componente e](changing-the-component-code.md) O que acontece se as regras do componente são [interrompidas?](what-happens-if-the-component-rules-are-broken.md)
3.  O instalador copia o arquivo de manifesto do assembly para a pasta que contém o arquivo especificado no campo Aplicativo de Arquivos da \_ [tabela MsiAssembly](msiassembly-table.md).
4.  Adicione uma linha à tabela [FeatureComponents,](featurecomponents-table.md) unindo o componente a um Windows instalador. Para obter mais informações, consulte [Componentes e recursos](components-and-features.md). Um Windows instalador deve ser uma parte da funcionalidade do aplicativo que um usuário pode reconhecer. O assembly é ativado quando esse recurso é selecionado por um usuário ou com falha em um aplicativo. Se o assembly definir um recurso adicional, adicione uma linha adicional à [tabela Recurso](feature-table.md) para os atributos do recurso. Esta etapa não será necessária se você estiver com um módulo de mesclagem.
5.  Para assemblies lado a lado, as informações de associação e ativação, por exemplo, classes COM, interfaces e bibliotecas de tipo, são armazenadas em arquivos de manifesto em vez do Registro. Assemblies privados armazenam essas informações em um manifesto do assembly. Em sistemas que suportam assemblies lado a lado, o instalador ignora o processamento de todas as informações sobre o componente inserido na tabela Extensão [,](extension-table.md) [tabela Verb](verb-table.md), [tabela TypeLib](typelib-table.md), [tabela MIME](mime-table.md), tabela [Class](class-table.md), [tabela ProgId](progid-table.md)e [tabela AppId](appid-table.md). Informações de associação e ativação podem ser inseridas nas tabelas para uso por sistemas que não suportam o compartilhamento de assembly lado a lado.
6.  A instalação lado a lado não registra o assembly globalmente. O instalador ignorará o auto-registro do componente se qualquer informação de autoregisão for inserida na [tabela SelfReg](selfreg-table.md). Informações de autoregisão podem ser inseridas na tabela SelfReg para auto-registro do componente em sistemas que não são suportados pelo compartilhamento de assembly lado a lado.
7.  Adicione outras informações do Registro, exclusivas da associação e da ativação ou do autoregiso do componente, à tabela Registro [,](registry-table.md)à tabela [RemoveRegistry e](removeregistry-table.md)à tabela [Ambiente](environment-table.md).
8.  O instalador ignora a tabela [IsolatedComponent](isolatedcomponent-table.md) para esse componente em sistemas operacionais que suportam o compartilhamento lado a lado. Insira informações nesta tabela se você quiser que o assembly seja privado em sistemas que deem suporte a arquivos locais.
9.  Adicione uma linha à [tabela MsiAssembly](msiassembly-table.md) para o componente que contém o assembly Win32. Insira um valor de 1 no campo Atributos da tabela MsiAssembly para especificar que este é um assembly Win32. Insira a chave de arquivo do assembly privado no campo Aplicativo \_ de Arquivo da tabela [MsiAssembly](msiassembly-table.md). Adicione a [ação MsiPublishAssemblies](msipublishassemblies-action.md) à tabela [InstallExecuteSequence](installexecutesequence-table.md) ou [à tabela AdvtExecuteSequence](advtexecutesequence-table.md). Adicione a [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md) à tabela InstallExecuteSequence. Autor de uma pasta para o assembly e o arquivo de manifesto na [tabela Diretório](directory-table.md). Essa pasta deve estar no diretório raiz do aplicativo e conter o arquivo especificado no campo Aplicativo de Arquivos da \_ [tabela MsiAssembly](msiassembly-table.md). Durante a instalação do aplicativo, o instalador resolve a tabela [Diretório](directory-table.md) para o caminho para essa pasta. Para obter mais informações, consulte [Usando a tabela de diretórios](using-the-directory-table.md).
10. Adicione linhas à tabela [MsiAssemblyName](msiassemblyname-table.md) para o componente. Adicione uma linha para cada par nome e valor especificado na seção assemblyIdentity do manifesto. Para obter mais informações, consulte [tabela MsiAssemblyName](msiassemblyname-table.md).

 

 



