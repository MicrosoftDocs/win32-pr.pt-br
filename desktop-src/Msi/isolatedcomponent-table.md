---
description: Cada registro da tabela IsolatedComponent associa o componente especificado na coluna Aplicativo de Componente (normalmente um .exe) ao componente especificado na coluna Component Shared (normalmente uma \_ \_ DLL compartilhada).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabela IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9644f1e122464e1321d55c0b615892167e84a7e059472adc4f01ee6bac571720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805614"
---
# <a name="isolatedcomponent-table"></a>Tabela IsolatedComponent

Cada registro da tabela IsolatedComponent associa o componente especificado na coluna Aplicativo de Componente (normalmente um .exe) ao componente especificado na coluna Component Shared (normalmente uma \_ \_ DLL compartilhada). A [ação IsolateComponents](isolatecomponents-action.md) instala uma cópia do Componente \_ Compartilhado em um local privado para uso pelo Aplicativo de \_ Componente. Isso isola o Aplicativo de Componente de outras cópias do Componente Compartilhado que podem \_ \_ ser instaladas em um local compartilhado no computador. Consulte [Componentes isolados](isolated-components.md).

Para vincular um componente compartilhado a vários aplicativos de componente, inclua um registro separado para cada par \_ \_ na tabela IsolatedComponents. O instalador copia os arquivos do Componente \_ Compartilhado no diretório de cada Aplicativo de Componente \_ instalado.

A tabela IsolatedComponent tem as seguintes colunas.



| Coluna                 | Tipo                         | Chave | Nullable |
|------------------------|------------------------------|-----|----------|
| Componente \_ Compartilhado      | [Identificador](identifier.md) | Y   | N        |
| Aplicativo \_ de componente | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ Compartilhado
</dt> <dd>

Chave estrangeira na [tabela Componente](component-table.md). O componente que contém o arquivo compartilhado, geralmente uma DLL. A DLL deve ser o arquivo de chave para esse componente. Esse deve ser um componente diferente do listado na coluna Aplicativo \_ de Componente.

O componente compartilhado controla o registro de todas as cópias isoladas do componente e deve ter o **sinalizador msidbComponentAttributesSharedDllRefCount** definido na coluna Atributos da tabela Component. Isso garante que o instalador possa gerenciar a vida útil do componente compartilhado.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Aplicativo \_ de componente
</dt> <dd>

Chave estrangeira na [tabela Componente](component-table.md). O componente que contém o .exe que carrega o arquivo compartilhado. O .exe deve ser o arquivo de chave para esse componente. Esse deve ser um componente diferente do listado na coluna Componente \_ Compartilhado.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE62](ice62.md)  
[ICE66](ice66.md)  
[ICE97](ice97.md)  
</dl>

 

 



