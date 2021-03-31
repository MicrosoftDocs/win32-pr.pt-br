---
description: A tabela UIText contém as versões localizadas de algumas das cadeias de caracteres usadas na interface do usuário. Essas cadeias de caracteres não fazem parte de nenhuma outra tabela. A tabela UIText é para cadeias de caracteres que não têm nenhum local lógico em nenhuma outra tabela.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Tabela UIText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089846"
---
# <a name="uitext-table"></a>Tabela UIText

A tabela UIText contém as versões localizadas de algumas das cadeias de caracteres usadas na interface do usuário. Essas cadeias de caracteres não fazem parte de nenhuma outra tabela. A tabela UIText é para cadeias de caracteres que não têm nenhum local lógico em nenhuma outra tabela.

A tabela UIText tem as colunas a seguir.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Chave    | [Identificador](identifier.md) | S   | N        |
| Texto   | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves
</dt> <dd>

Uma chave exclusiva que identifica a cadeia de caracteres específica.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

A versão localizada da cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Alguns controles usam a tabela UIText como uma fonte de cadeias de caracteres. Para obter informações sobre quais cadeias de caracteres são necessárias nesta tabela para cada controle específico, consulte os controles individuais na [referência da interface do usuário](user-interface-reference.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



