---
description: A tabela TypeLib contém as informações que precisam ser colocadas no registro do registro de bibliotecas de tipos.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Tabela TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862bc37e325f8c615e8158cfa431c927841f6b33c403c804726cea8fee6f0469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499996"
---
# <a name="typelib-table"></a>Tabela TypeLib

A tabela TypeLib contém as informações que precisam ser colocadas no registro do registro de bibliotecas de tipos.

A tabela TypeLib tem as colunas a seguir.



| Coluna      | Tipo                               | Chave | Nullable |
|-------------|------------------------------------|-----|----------|
| LibID       | [GUID](guid.md)                   | Y   | N        |
| Idioma    | [Inteiro](integer.md)             | Y   | N        |
| Componente\_ | [Identificador](identifier.md)       | Y   | N        |
| Versão     | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Descrição | [Text](text.md)                   | N   | Y        |
| Diretório\_ | [Identificador](identifier.md)       | N   | Y        |
| Recurso\_   | [Identificador](identifier.md)       | N   | N        |
| Custo        | [DoubleInteger](doubleinteger.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID
</dt> <dd>

O GUID que identifica a biblioteca.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma
</dt> <dd>

O idioma da biblioteca de tipos. Este deve ser um número não negativo.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [componentes](component-table.md). Esta coluna identifica o componente pertencente ao recurso \_ cujo arquivo de chave é a biblioteca de tipos que está sendo registrada.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versão
</dt> <dd>

Esta é a versão da biblioteca. As versões principal e secundária são codificadas no valor inteiro de quatro bytes. A versão secundária está nos oito bits inferiores. A versão principal está no meio dos dezesseis bits.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Uma descrição localizável da biblioteca.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [diretórios](directory-table.md). Esta coluna identifica o caminho de ajuda para a biblioteca de tipos. Esta coluna é ignorada durante o anúncio.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Chave externa na primeira coluna da tabela de [recursos](feature-table.md). Esta coluna especifica o recurso que deve ser instalado para que a biblioteca de tipos esteja operacional.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Custo
</dt> <dd>

O custo associado ao registro da biblioteca de tipos em bytes. Este deve ser um número não negativo ou nulo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referida quando a ação [RegisterTypeLibraries](registertypelibraries-action.md) ou a [ação UnregisterTypeLibraries](unregistertypelibraries-action.md) é executada.

O instalador grava todas as informações de registro da biblioteca de tipos no \_ \_ local do registro da máquina local hKey (HKLM). Esse é o caso até mesmo para instalações por usuário. Bibliotecas de tipos não podem ser registradas em locais por usuário (HKCU).

Os autores do pacote de instalação são altamente aconselhados em relação ao uso da tabela TypeLib. Em vez disso, eles devem registrar bibliotecas de tipos usando a tabela de [registro](registry-table.md) . Os motivos para evitar o auto-registro incluem:

-   Se uma instalação que usa a tabela TypeLib falhar e precisar ser revertida, a reversão poderá não restaurar o computador para o mesmo estado que existia antes da reversão. Bibliotecas de tipos registradas antes da reversão não podem ser registradas após a reversão.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
</dl>

 

 



