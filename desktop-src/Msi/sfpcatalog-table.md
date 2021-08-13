---
description: A tabela SFPCatalog contém os catálogos usados pelo Windows Me.
ms.assetid: e9dc65a9-4ec9-4310-b03a-a2c38720ca8c
title: Tabela SFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97498ff6437967a4a588be7b957aea130dad201699d55fad3abace6ff094b271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624887"
---
# <a name="sfpcatalog-table"></a>Tabela SFPCatalog

A tabela SFPCatalog contém os catálogos usados pelo Windows Me.

A tabela SFPCatalog tem as seguintes colunas.



| Coluna     | Tipo                       | Chave | Nullable |
|------------|----------------------------|-----|----------|
| SFPCatalog | [Filename](filename.md)   | Y   | N        |
| Catálogo    | [Binary](binary.md)       | N   | N        |
| Dependência | [Formatado](formatted.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="SFPCatalog"></span><span id="sfpcatalog"></span><span id="SFPCATALOG"></span>SFPCatalog
</dt> <dd>

O nome de arquivo curto para o catálogo. Como os catálogos não têm nenhuma versão, o catálogo especificado nesta coluna pode substituir um catálogo que tem o mesmo nome e já está instalado no sistema local. Consulte o tópico de versão do arquivo [Nenhum arquivo tem uma versão](neither-file-has-a-version.md).

</dd> <dt>

<span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo
</dt> <dd>

Dados binários para o catálogo.

</dd> <dt>

<span id="Dependency"></span><span id="dependency"></span><span id="DEPENDENCY"></span>Dependência
</dt> <dd>

O catálogo especificado nesse campo é o pai do catálogo dependente especificado no campo SFPCatalog. Insira o nome de arquivo curto do catálogo pai no campo Dependência. Esse campo é uma chave de volta para a coluna SFPCatalog. A combinação de dependências é sensível a minúsculas.

Se o campo Dependência referenciar outro registro nesta tabela SFPCatalog, o catálogo pai será instalado antes do catálogo dependente.

Se o campo Dependência fizer referência a um catálogo pai que não está presente no campo SFPCatalog desta tabela e se o catálogo pai ainda não estiver instalado, a instalação falhará.

</dd> </dl>

## <a name="remarks"></a>Comentários

A [ação InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta a tabela [Component](component-table.md) [,](file-table.md)a tabela File , a tabela [FileSFPCatalog](filesfpcatalog-table.md) e a tabela SFPCatalog.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
</dl>

 

 



