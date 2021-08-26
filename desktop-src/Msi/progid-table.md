---
description: A tabela ProgId contém informações para IDs de programa e IDs de programa independentes de versão que devem ser geradas como parte do anúncio do produto.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Tabela ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed8baea9bd8421757cf2e31f0ba06679db3394c95f732537a7e230c02b5ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042056"
---
# <a name="progid-table"></a>Tabela ProgId

A tabela ProgId contém informações para IDs de programa e IDs de programa independentes de versão que devem ser geradas como parte do anúncio do produto.

A tabela ProgId tem as colunas a seguir.



| Coluna         | Tipo                         | Chave | Nullable |
|----------------|------------------------------|-----|----------|
| ProgId         | [Text](text.md)             | Y   | N        |
| Pai do ProgId \_ | [Text](text.md)             | N   | Y        |
| Classe\_        | [GUID](guid.md)             | N   | Y        |
| Descrição    | [Text](text.md)             | N   | Y        |
| Ícone\_         | [Identificador](identifier.md) | N   | Y        |
| IconIndex      | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId
</dt> <dd>

A ID do programa ou a ID do programa independente da versão. Os ProgIds listados na tabela ProgId serão registrados se o CLSID listado na coluna classe \_ desta tabela estiver agendado para ser anunciado ou instalado. Quando o ProgId é selecionado para registro, todos os ProgIds que se referem a essa linha por meio da \_ coluna pai ProgID também são selecionados para registro.

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>Pai do ProgId \_
</dt> <dd>

Definido somente para IDs de programa independentes de versão. Esse campo é uma chave estrangeira na coluna ProgId. Para definir uma ID de programa independente de versão, insira o ProgId correspondente na \_ coluna pai do ProgID. Quando o ProgId é selecionado para instalação, os ProgIds independentes de versão correspondentes associados por meio da \_ coluna pai do ProgID também são selecionados para registro.

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Classes\_
</dt> <dd>

Uma chave estrangeira opcional na [tabela de classes](class-table.md). Esta coluna deve ser nula para uma ProgId independente de versão. Se o valor de classe \_ de um ProgID for nulo, o ProgID será registrado quando aparecer na coluna ProgID de uma linha na tabela de [extensão](extension-table.md) e a extensão tiver pelo menos um verbo associado a ele na tabela de [verbos](verb-table.md). ProgIds selecionados para registro dessa maneira não instalam outros ProgIds que referenciam a ProgId atual por meio do \_ valor padrão de ProgID.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Uma descrição opcional localizada da ID do programa associada.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Cone\_
</dt> <dd>

Uma chave estrangeira opcional na [tabela de ícones](icon-table.md) que especifica o arquivo de ícone associado a este ProgID. Isso é escrito sob a chave DefaultIcon associada a este ProgId. Esta coluna deve ser nula para uma ProgId independente de versão.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

O índice de ícone no arquivo de ícone. Esta coluna deve ser nula para uma ProgId independente de versão.

</dd> </dl>

## <a name="remarks"></a>Comentários

As ações [RegisterProgIdInfo](registerprogidinfo-action.md) e [UnregisterProgIdInfo](unregisterprogidinfo-action.md) nas [*tabelas de sequência*](s-gly.md) processam as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



