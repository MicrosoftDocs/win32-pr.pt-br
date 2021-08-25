---
description: A tabela CCPSearch contém a lista de assinaturas de arquivo usadas para o CCP (Programa de Verificação de Conformidade). Pelo menos um desses arquivos precisa estar presente no computador de um usuário para que o usuário seja em conformidade com o programa.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Tabela CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d20894960dce7f346601bd2ed459140caa305323ca02d14d54416f32737216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821836"
---
# <a name="ccpsearch-table"></a>Tabela CCPSearch

A tabela CCPSearch contém a lista de assinaturas de arquivo usadas para o CCP (Programa de Verificação de Conformidade). Pelo menos um desses arquivos precisa estar presente no computador de um usuário para que o usuário seja em conformidade com o programa.

A tabela CCPSearch tem a coluna a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Assinatura\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="column"></a>Coluna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Assinatura\_
</dt> <dd>

A Assinatura representa uma assinatura de arquivo exclusiva e também é a chave externa nas tabelas \_ [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator,](inilocator-table.md) [CompLocator](complocator-table.md)e [DrLocator.](drlocator-table.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referenciada quando a [ação CCPSearch](ccpsearch-action.md) ou [a ação RMCCPSearch](rmccpsearch-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



