---
description: Windows os desenvolvedores de instalador podem usar as diretrizes neste tópico para criar Windows Installer pacotes que contêm assemblies.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Adicionando assemblies a um pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a96c1b8c8d9b73fedf03fceeb82be62b8457556da02334ed7a224aefc2202a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534866"
---
# <a name="adding-assemblies-to-a-package"></a>Adicionando assemblies a um pacote

Windows os desenvolvedores de instalador podem usar as diretrizes neste tópico para criar Windows Installer pacotes que contêm assemblies.

as diretrizes a seguir se aplicam a assemblies do Win32 e assemblies que o Common Language Runtime do Microsoft .NET Framework usa.

-   um componente Windows Installer não deve conter mais de um assembly.
-   Todos os arquivos no assembly devem estar em um único componente.
-   Cada componente que contém um assembly deve ter uma entrada na tabela [MsiAssembly](msiassembly-table.md) .
-   O nome de cache de assembly forte de cada assembly deve ser criado na tabela [MsiAssemblyName](msiassemblyname-table.md) .
-   Use a tabela de [registro](registry-table.md) em vez da tabela de [classes](class-table.md) ao registrar a interoperabilidade com para um assembly.
-   Os assemblies que têm o mesmo nome forte são o mesmo assembly. Quando o mesmo assembly é instalado por aplicativos diferentes, os componentes que contêm o assembly devem usar o mesmo valor para o ComponentID em suas tabelas de [componentes](component-table.md) .

> [!Note]  
> Anúncios de produtos identificam assemblies que podem ser instalados e usados por diferentes aplicativos. Os anúncios de produtos não identificam assemblies privados.

 

## <a name="adding-win32-assemblies"></a>Adicionando assemblies Win32

Use as seguintes diretrizes ao incluir assemblies Win32:

-   O valor KeyPath na tabela de [componentes](component-table.md) para um componente que contém um assembly Win32 não deve ser nulo.
-   O valor KeyPath na tabela de [componentes](component-table.md) para um componente que contém um assembly de política do Win32 deve ser o arquivo de manifesto.
-   O valor KeyPath na tabela de [componentes](component-table.md) para um componente que contém um assembly Win32, que não é um assembly de política, não deve ser o arquivo de manifesto ou arquivo de catálogo. Deve ser um arquivo diferente no assembly.
-   Adicione uma linha à tabela [MsiAssemblyName](msiassemblyname-table.md) para cada par de nome e valor listado na seção **AssemblyIdentity** do manifesto do assembly Win32.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Adicionando assemblies usados com o .NET Framework

Use as diretrizes a seguir ao incluir assemblies que o Common Language Runtime do .NET Framework usa.

-   O valor KeyPath na tabela de [componentes](component-table.md) para um componente que contém o assembly não deve ser nulo.
-   Quando você instala um assembly usado pelo Common Language Runtime para o cache de assembly global, o valor na \_ coluna aplicativo de arquivo da tabela MsiAssembly deve ser nulo.
-   Adicione uma linha à tabela [MsiAssemblyName](msiassemblyname-table.md) para cada atributo do nome forte do assembly. Todos os assemblies devem ter o nome, a versão e os atributos de cultura especificados na tabela MsiAssemblyName. Um atributo publicKeyToken é necessário para um assembly global. A tabela a seguir é um exemplo da tabela MsiAssemblyName para um assembly global para uso pelo Common Language Runtime.

[Tabela MsiAssemblyName](msiassemblyname-table.md)



| Componente  | Nome           | Valor            |
|------------|----------------|------------------|
| Componente | Nome           | simple           |
| Componente | version        | 1.0.0.0          |
| Componente | Cultura        | neutro          |
| Componente | publicKeyToken | 9d1ec8380f483f5a |



 

 

 



