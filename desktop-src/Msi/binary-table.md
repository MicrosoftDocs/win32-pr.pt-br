---
description: A tabela binária contém os dados binários de itens como bitmaps, animações e ícones. A tabela binária também é usada para armazenar dados para ações personalizadas. consulte limitações de OLE em Fluxos.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabela binária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a70750193b1dc147a9b2b4cfa01bbea410f0e44b7c03f16bd1c992f118a4f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638800"
---
# <a name="binary-table"></a>Tabela binária

A tabela binária contém os dados binários de itens como bitmaps, animações e ícones. A tabela binária também é usada para armazenar dados para ações personalizadas. consulte [limitações de OLE em Fluxos](ole-limitations-on-streams.md).

A tabela binária tem as colunas a seguir.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Nome   | [Identificador](identifier.md) | Y   | N        |
| Dados   | [Binary](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Uma chave exclusiva que identifica os dados binários específicos. Se os dados binários forem para um controle, a chave aparecerá na coluna de texto do controle associado na [tabela de controle](control-table.md). Essa chave deve ser exclusiva entre todos os controles que exigem dados binários.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado
</dt> <dd>

Os dados binários não formatados.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE29](ice29.md)  
</dl>

 

 



