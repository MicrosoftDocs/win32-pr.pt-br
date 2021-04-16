---
description: Cada registro da tabela IsolatedComponent associa o componente especificado na \_ coluna aplicativo de componente (normalmente um. exe) com o componente especificado na \_ coluna compartilhada componente (normalmente, uma DLL compartilhada).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabela IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759220"
---
# <a name="isolatedcomponent-table"></a>Tabela IsolatedComponent

Cada registro da tabela IsolatedComponent associa o componente especificado na \_ coluna aplicativo de componente (normalmente um. exe) com o componente especificado na \_ coluna compartilhada componente (normalmente, uma DLL compartilhada). A [ação IsolateComponents](isolatecomponents-action.md) instala uma cópia do componente \_ compartilhado em um local privado para uso por aplicativo de componente \_ . Isso isola o aplicativo de componente \_ de outras cópias de componentes \_ compartilhados que podem ser instalados em um local compartilhado no computador. Consulte [componentes isolados](isolated-components.md).

Para vincular um componente \_ compartilhado a vários aplicativos de componente \_ , inclua um registro separado para cada par na tabela IsolatedComponents. O instalador copia os arquivos do componente \_ compartilhado para o diretório de cada aplicativo de componente \_ que está instalado.

A tabela IsolatedComponent tem as colunas a seguir.



| Coluna                 | Tipo                         | Chave | Nullable |
|------------------------|------------------------------|-----|----------|
| Componente \_ compartilhado      | [Identificador](identifier.md) | S   | N        |
| Aplicativo de componente \_ | [Identificador](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ compartilhado
</dt> <dd>

Chave estrangeira na [tabela de componentes](component-table.md). O componente que contém o arquivo compartilhado, geralmente uma DLL. A DLL deve ser o arquivo de chave para esse componente. Ele deve ser um componente diferente do listado na \_ coluna aplicativo de componente.

O componente compartilhado controla o registro de todas as cópias isoladas do componente e deve ter o sinalizador **msidbComponentAttributesSharedDllRefCount** definido na coluna atributos da tabela de componentes. Isso garante que o instalador possa gerenciar a vida útil do componente compartilhado.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Aplicativo de componente \_
</dt> <dd>

Chave estrangeira na [tabela de componentes](component-table.md). O componente que contém o. exe que carrega o arquivo compartilhado. O. exe deve ser o arquivo de chave para esse componente. Ele deve ser um componente diferente do listado na \_ coluna compartilhada do componente.

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

 

 



