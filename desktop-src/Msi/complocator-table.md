---
description: A tabela CompLocator contém as informações necessárias para encontrar um arquivo ou diretório que está usando os dados de configuração do instalador.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Tabela CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6a51ad618521ff49b2a5b13f76fcfbae4207b5cdf4d77e76d3e128816bbb82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145075"
---
# <a name="complocator-table"></a>Tabela CompLocator

A tabela CompLocator contém as informações necessárias para encontrar um arquivo ou diretório que está usando os dados de configuração do instalador.

A tabela CompLocator contém as informações a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Assinatura\_ | [Identificador](identifier.md) | Y   | N        |
| Componentid | [GUID](guid.md)             | N   | N        |
| Tipo        | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="column-information"></a>Informações da coluna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Assinatura\_
</dt> <dd>

Essa coluna representa uma assinatura de arquivo exclusiva e também é a chave externa na [Tabela de Assinatura](signature-table.md). Se a chave estiver ausente da Tabela de Assinatura, supõe-se que a pesquisa seja para a presença de um diretório apontado pela tabela CompLocator.

</dd> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

A ID do componente cujo caminho de chave deve ser usado para a pesquisa. Esse deve ser o GUID de um componente que aparece no campo ComponentId da [Tabela de Componentes](component-table.md). Pode ser a ID do componente de um componente que pertence a outro produto instalado no computador. Ele não deve ser o GUID de um componente publicado que aparece no campo ComponentId da [Tabela PublishComponent](publishcomponent-table.md).

Para encontrar o valor do GUID da ID do componente para um arquivo instalado por outro produto, acesse o pacote de instalação do produto. Vá para a [Tabela de Arquivos](file-table.md) e encontre a linha que contém o identificador de arquivo para o arquivo. A coluna \_ Componente desta linha contém o identificador de componente para o componente que controla o arquivo. Vá para a [tabela Componente e](component-table.md) encontre a linha que contém esse identificador de componente na coluna Componente. A coluna ComponentId dessa linha contém o GUID da ID do componente.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Um valor booliana que determina se o caminho da chave do componente é um nome de arquivo ou um local de diretório.

A tabela a seguir lista valores válidos. Se ausente, Type será definido como 1 (um).



| Constante                      | Hexadecimal | Decimal | Descrição              |
|-------------------------------|-------------|---------|--------------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | O caminho da chave é um diretório. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | O caminho da chave é um nome de arquivo. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta tabela é usada com a [tabela AppSearch](appsearch-table.md).

Normalmente, as colunas nesta tabela não são localizadas. Se um autor decidir pesquisar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.

Para obter mais informações, consulte [Procurando aplicativos existentes, arquivos,](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)entradas do Registro ou .ini de arquivo .

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



