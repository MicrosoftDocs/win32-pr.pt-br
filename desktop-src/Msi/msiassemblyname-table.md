---
description: A tabela MsiAssembly e a tabela MsiAssemblyName especificam Windows Installer configurações para assemblies de Common Language Runtime e assemblies do Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Tabela MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783268"
---
# <a name="msiassemblyname-table"></a>Tabela MsiAssemblyName

A tabela [MsiAssembly](msiassembly-table.md) e a tabela MsiAssemblyName especificam Windows Installer configurações para assemblies de Common Language Runtime e assemblies do Win32. Para obter informações, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e [instalação de assemblies do Win32](installation-of-win32-assemblies.md).

A tabela MsiAssemblyName especifica o esquema para os elementos de um nome de cache de assembly forte para um assembly .NET Framework ou Win32. O nome é construído acrescentando todos os elementos com a mesma chave de componente \_ . Veja o exemplo a seguir.

Windows Installer pode instalar assemblies do Win32 como [assemblies lado a lado](side-by-side-assemblies.md). Para obter mais informações, consulte a [API do assembly lado a lado](../sbscs/side-by-side-assembly-api.md).

A tabela MsiAssemblyName tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificador](identifier.md) | S   | N        |
| Nome        | [Text](text.md)             | S   | N        |
| Valor       | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

A chave na [tabela de componentes](component-table.md) que especifica o componente de Windows Installer que contém esse assembly.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Nome do atributo associado ao valor especificado na coluna valor.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

Valor associado ao nome especificado na coluna nome.

</dd> </dl>

## <a name="remarks"></a>Comentários

As informações criadas na tabela MsiAssemblyName devem corresponder às informações no arquivo de manifesto do assembly. Se as informações no manifesto e na tabela MsiAssemblyName não corresponderem, a remoção do aplicativo poderá deixar o assembly no computador.

Para assemblies do Win32, deve haver uma linha na tabela MsiAssemblyName para cada uma das seguintes entradas no campo Nome: tipo, nome, versão, idioma, publicKeyToken e processorArchitecture. O valor correspondente para cada nome pode ser inserido no campo valor. Os pares de nome-valor na tabela MsiAssemblyName devem corresponder aos atributos Type, Name, Version, language, publicKeyToken e processorArchitecture no manifesto do assembly.

Para assemblies de Common Language Runtime privada (.NET Frameworkversions 1,0 e 1,1), a tabela MsiAssemblyName deve incluir uma linha para cada uma das seguintes entradas no campo Nome: nome, versão e cultura. O valor correspondente para cada nome pode ser inserido no campo valor.

Para assemblies de Common Language Runtime global (.NET Framework versões 1,0 e 1,1), a tabela MsiAssemblyName deve incluir uma linha para cada uma das seguintes entradas no campo Nome: nome, versão, cultura e PublicKeyToken. O valor correspondente para cada nome pode ser inserido no campo valor.

A versão .NET Framework 1,1 é a versão mínima que pode ser usada para executar uma atualização in-loco de um assembly de Common Language Runtime global. Você pode verificar a propriedade [**MsiNetAssemblySupport**](msinetassemblysupport.md) para a versão. A tabela MsiAssemblyName também deve ter um campo FileVersion porque esse tipo de atualização de assembly altera apenas o FileVersion. Para obter mais informações, consulte [atualizando assemblies](updating-assemblies.md).

Por exemplo, o manifesto do assembly para componenteA pode ter uma seção assemblyIdentity da seguinte maneira para um assembly Win32.

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

Nesse caso, preencha a tabela MsiAssemblyName da seguinte maneira.



| Componente  | Nome                  | Valor             |
|------------|-----------------------|-------------------|
| Componente | tipo                  | Win32             |
| Componente | name                  | MS-sxstest-simples |
| Componente | version               | 1.0.0.0           |
| Componente | Linguagem              | en                |
| Componente | publicKeyToken        | 1111111111222222  |
| Componente | processorArchitecture | x86               |



 

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE83](ice83.md)  
</dl>

 

 
