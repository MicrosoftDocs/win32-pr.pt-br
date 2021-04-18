---
description: A tabela binária contém os dados binários de itens como bitmaps, animações e ícones. A tabela binária também é usada para armazenar dados para ações personalizadas. Consulte limitações de OLE em fluxos.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Tabela binária
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778732"
---
# <a name="binary-table"></a>Tabela binária

A tabela binária contém os dados binários de itens como bitmaps, animações e ícones. A tabela binária também é usada para armazenar dados para ações personalizadas. Consulte [limitações de OLE em fluxos](ole-limitations-on-streams.md).

A tabela binária tem as colunas a seguir.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Nome   | [Identificador](identifier.md) | S   | N        |
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

 

 



