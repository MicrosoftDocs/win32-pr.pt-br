---
description: A tabela MsiPatchHeaders contém os fluxos de header de patch binários usados para validação de patch.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabela MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1888a91da13923c4a9904c770df77cb24a5b8381c869a60895bb5ff49d23e6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944484"
---
# <a name="msipatchheaders-table"></a>Tabela MsiPatchHeaders

A tabela MsiPatchHeaders contém os fluxos de header de patch binários usados para validação de patch.

A tabela MsiPatchHeaders é [](file-table.md) usada quando chaves de tabela de arquivo longas resultam em uma falha ao gerar o fluxo de header de patch na [tabela Patch](patch-table.md). Isso pode ser devido à limitação do nome do fluxo descrita em [Limitações OLE no Fluxos](ole-limitations-on-streams.md). Nesse caso, a tabela Patch pode referenciar a tabela MsiPatchHeaders para criar o fluxo de header de patch.

A tabela MsiPatchHeaders tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| StreamRef | [Identificador](identifier.md) | Y   | N        |
| Cabeçalho    | [Binary](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

A chave primária da tabela que identifica exclusivamente um determinado header de patch.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Cabeçalho
</dt> <dd>

Esta coluna é o header de patch de fluxo binário usado para validação de patch.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é processada pela [ação PatchFiles](patchfiles-action.md). Essa tabela geralmente é adicionada ao pacote de instalação por uma transformação de um pacote de patch. Normalmente, ele não é feito diretamente em um pacote de instalação.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



