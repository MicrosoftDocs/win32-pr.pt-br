---
description: A Tabela MsiAssembly especifica Windows do Instalador para assemblies do Microsoft .NET Framework e assemblies Win32. Para obter mais informações, consulte Instalação de assemblies no cache de assembly global e instalação de assemblies Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabela MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda246bd6baba75d0f7e8d53f515a25abb0c163c2d3ef0b1b9705c123b8e69e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381376"
---
# <a name="msiassembly-table"></a>Tabela MsiAssembly

A Tabela MsiAssembly especifica Windows do Instalador para assemblies do Microsoft .NET Framework e assemblies Win32. Para obter mais informações, [consulte Instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e instalação de [assemblies Win32](installation-of-win32-assemblies.md).

No Windows XP, Windows instalador pode instalar assemblies Win32 como [assemblies lado a lado.](side-by-side-assemblies.md) Para obter mais informações, consulte a API de assembly lado [a lado.](../sbscs/side-by-side-assembly-api.md)

**Windows 2000:** Não há suporte para esse recurso.

A Tabela MsiAssembly tem as seguintes colunas.



| Coluna            | Tipo                         | Chave | Nullable |
|-------------------|------------------------------|-----|----------|
| Componente\_       | [Identificador](identifier.md) | Y   | N        |
| Recurso\_         | [Identificador](identifier.md) | N   | N        |
| Manifesto do \_ arquivo    | [Identificador](identifier.md) | N   | Y        |
| Aplicativo de \_ arquivo | [Identificador](identifier.md) | N   | Y        |
| Atributos        | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

A chave na Tabela [de Componentes](component-table.md) que especifica o componente Windows Instalador que contém esse assembly.

O valor nesse campo não deve ser definido como nulo. O campo KeyPath do componente na [Tabela de Componentes](component-table.md) não deve ser nulo.

Para assemblies Win32, o componente KeyPath não pode ser o arquivo de manifesto especificado no Manifesto do \_ Arquivo. O manifesto pode ser o caminho da chave para um assembly de .NET Framework ou de política.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Chave na Tabela [de Recursos](feature-table.md).

Quando o assembly deve ser instalado por uma instalação de recurso, Windows Instalador instala o recurso apontado por esse campo.

</dd> <dt>

<span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifesto do \_ arquivo
</dt> <dd>

Uma chave externa na Tabela [de Arquivos](file-table.md) que especifica o arquivo que contém o manifesto para um assembly .NET Framework ou assembly Win32.

Para um assembly Win32, não especifique esse arquivo como o arquivo de caminho da chave do componente no campo KeyPath da [Tabela de Componentes](component-table.md).

</dd> <dt>

<span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Aplicativo de \_ arquivo
</dt> <dd>

Para instalar o assembly em um local privado, insira o arquivo de caminho de chave para o componente de assembly neste campo.

Esse é o valor que aparece no campo KeyPath da [Tabela de Componentes](component-table.md). O Instalador pode instalar o assembly na estrutura de diretório do componente especificado na Tabela [de Diretórios](directory-table.md). Esse campo deverá ser nulo se o assembly for instalado no cache de assembly global.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Insira um valor de 1 (um) para um assembly Win32. Insira um valor de 0 (zero) para um .NET Framework assembly.

Se a coluna Atributos for NULL, o Instalador tratará o assembly como um assembly .NET Framework assembly.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se houver pelo menos uma entrada na Tabela MsiAssembly, a Tabela [InstallExecuteSequence](installexecutesequence-table.md) deverá conter a Ação [MsiPublishAssemblies](msipublishassemblies-action.md)e a [Ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md).

Como os assemblies não podem ser retordenados depois que são confirmados, Windows Instalador usa um processo de instalação em duas etapas. As interfaces para os assemblies são criadas durante as operações de instalação geradas pela [Ação MsiPublishAssemblies](msipublishassemblies-action.md).

Os assemblies não são comprometidos até que a execução bem-sucedida da [Ação InstallFinalize seja bem-sucedida.](installfinalize-action.md) Isso significa que, se você tiver uma ação personalizada ou recurso que se baseia no assembly, ele deverá ser sequenciado após a [Ação InstallFinalize](installfinalize-action.md). Por exemplo, se você precisar iniciar um serviço que depende de um assembly no GAC (Cache de Assembly Global), deverá agendar o início desse serviço após a [Ação InstallFinalize](installfinalize-action.md). Isso significa que você não pode usar a [Tabela ServiceControl](servicecontrol-table.md) para iniciar o serviço, em vez disso, você deve usar uma ação personalizada que é sequenciada após InstallFinalize.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
[ICE94](ice94.md)  
</dl>

 

 
