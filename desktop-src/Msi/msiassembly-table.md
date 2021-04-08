---
description: A tabela MsiAssembly especifica Windows Installer configurações para assemblies do Microsoft .NET Framework e assemblies do Win32. Para obter mais informações, consulte instalação de assemblies no cache de assembly global e instalação de assemblies do Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabela MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922816"
---
# <a name="msiassembly-table"></a>Tabela MsiAssembly

A tabela MsiAssembly especifica Windows Installer configurações para assemblies do Microsoft .NET Framework e assemblies do Win32. Para obter mais informações, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e [instalação de assemblies do Win32](installation-of-win32-assemblies.md).

No Windows XP, Windows Installer pode instalar assemblies do Win32 como [assemblies lado a lado](side-by-side-assemblies.md). Para obter mais informações, consulte a [API do assembly lado a lado](../sbscs/side-by-side-assembly-api.md).

**Windows 2000:** Não há suporte para esse recurso.

A tabela MsiAssembly tem as colunas a seguir.



| Coluna            | Tipo                         | Chave | Nullable |
|-------------------|------------------------------|-----|----------|
| Componente\_       | [Identificador](identifier.md) | S   | N        |
| Recurso\_         | [Identificador](identifier.md) | N   | N        |
| Manifesto do arquivo \_    | [Identificador](identifier.md) | N   | S        |
| Aplicativo de arquivo \_ | [Identificador](identifier.md) | N   | S        |
| Atributos        | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

A chave na [tabela de componentes](component-table.md) que especifica o componente de Windows Installer que contém esse assembly.

O valor neste campo não deve ser definido como nulo. O campo caminho do componente na [tabela de componentes](component-table.md) não deve ser nulo.

Para assemblies do Win32, o caminho KeyPath não pode ser o arquivo de manifesto especificado no \_ manifesto do arquivo. O manifesto pode ser o caminho Keypara um .NET Framework ou assembly de política.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

A chave na [tabela de recursos](feature-table.md).

Quando o assembly deve ser instalado por uma instalação de recurso, Windows Installer instala o recurso apontado por esse campo.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifesto do arquivo \_
</dt> <dd>

Uma chave externa na [tabela de arquivos](file-table.md) que especifica o arquivo que contém o manifesto para um assembly .NET Framework ou assembly Win32.

Para um assembly Win32, não especifique esse arquivo como o arquivo de caminho de chave de componente no campo KeyPath da [tabela de componentes](component-table.md).

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Aplicativo de arquivo \_
</dt> <dd>

Para instalar o assembly em um local privado, insira o arquivo de caminho de chave para o componente de assembly neste campo.

Esse é o valor que aparece no campo KeyPath da tabela de [componentes](component-table.md). O instalador pode instalar o assembly na estrutura de diretório do componente especificado na [tabela de diretórios](directory-table.md). Esse campo deverá ser nulo se o assembly for instalado no cache de assembly global.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Insira um valor de 1 (um) para um assembly Win32. Insira um valor de 0 (zero) para um assembly .NET Framework.

Se a coluna Attributes for nula, o instalador tratará o assembly como um assembly .NET Framework.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se houver pelo menos uma entrada na tabela MsiAssembly, a [tabela InstallExecuteSequence](installexecutesequence-table.md) deverá conter a [ação MsiPublishAssemblies](msipublishassemblies-action.md)e a [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

Como os assemblies não podem ser revertidos depois de serem confirmados, Windows Installer usa um processo de instalação em duas etapas. As interfaces para os assemblies são criadas durante as operações de instalação geradas pela [ação MsiPublishAssemblies](msipublishassemblies-action.md).

Os assemblies não são confirmados até a execução bem-sucedida da [ação InstallFinalize](installfinalize-action.md). Isso significa que, se você criar uma ação personalizada ou um recurso que dependa do assembly, ele deverá ser sequenciado após a [ação InstallFinalize](installfinalize-action.md). Por exemplo, se você precisar iniciar um serviço que depende de um assembly no GAC (cache de assembly global), será necessário agendar o início desse serviço após a [ação InstallFinalize](installfinalize-action.md). Isso significa que você não pode usar a [tabela de UserControl](servicecontrol-table.md) para iniciar o serviço, em vez disso, você deve usar uma ação personalizada que é sequenciada após InstallFinalize.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
