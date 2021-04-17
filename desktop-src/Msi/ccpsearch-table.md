---
description: A tabela CCPSearch contém a lista de assinaturas de arquivo usadas para o CCP (programa de verificação de conformidade). Pelo menos um desses arquivos precisa estar presente no computador de um usuário para que o usuário esteja em conformidade com o programa.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Tabela CCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770383"
---
# <a name="ccpsearch-table"></a>Tabela CCPSearch

A tabela CCPSearch contém a lista de assinaturas de arquivo usadas para o CCP (programa de verificação de conformidade). Pelo menos um desses arquivos precisa estar presente no computador de um usuário para que o usuário esteja em conformidade com o programa.

A tabela CCPSearch tem a seguinte coluna.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificador](identifier.md) | S   | N        |



 

## <a name="column"></a>Coluna

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

A assinatura \_ representa uma assinatura de arquivo exclusiva e também é a chave externa nas tabelas [Signature](signature-table.md), [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)e [DrLocator](drlocator-table.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referida quando a ação [CCPSearch](ccpsearch-action.md) ou a [ação RMCCPSearch](rmccpsearch-action.md) é executada.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



