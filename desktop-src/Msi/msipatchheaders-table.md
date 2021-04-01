---
description: A tabela MsiPatchHeaders contém os fluxos de cabeçalho de patch binários usados para validação de patch.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabela MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169847"
---
# <a name="msipatchheaders-table"></a>Tabela MsiPatchHeaders

A tabela MsiPatchHeaders contém os fluxos de cabeçalho de patch binários usados para validação de patch.

A tabela MsiPatchHeaders é usada quando chaves de [tabela de arquivos](file-table.md) longos resultam em uma falha ao gerar o fluxo de cabeçalho de patch na tabela de [patches](patch-table.md). Isso pode ser devido à limitação de nome de fluxo descrita em [limitações de OLE em fluxos](ole-limitations-on-streams.md). Nesse caso, a tabela de patch pode fazer referência à tabela MsiPatchHeaders para criar o fluxo de cabeçalho de patch.

A tabela MsiPatchHeaders tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| StreamRef | [Identificador](identifier.md) | S   | N        |
| parâmetro    | [Binary](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

A chave primária da tabela que identifica exclusivamente um cabeçalho de patch específico.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Verga
</dt> <dd>

Esta coluna é o cabeçalho de patch de fluxo binário usado para validação de patch.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é processada pela [ação PatchFiles](patchfiles-action.md). Normalmente, essa tabela é adicionada ao pacote de instalação por uma transformação de um pacote de patch. Normalmente, ele não é criado diretamente em um pacote de instalação.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



