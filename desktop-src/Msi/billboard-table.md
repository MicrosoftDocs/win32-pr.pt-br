---
description: A tabela de mural lista os controles de mural exibidos na interface do usuário completa.
ms.assetid: bb8c1d7c-aa1d-43cc-9fb4-3a0ad75c4615
title: Tabela de mural
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a561eb629e07b25437d6e5ce12b58bb0d7dd20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921485"
---
# <a name="billboard-table"></a>Tabela de mural

A tabela de mural lista os [controles de mural](billboard-control.md) exibidos na interface do usuário completa.

A tabela de mural tem as colunas a seguir.



| Coluna    | Tipo                         | Chave | Nullable |
|-----------|------------------------------|-----|----------|
| Mensagem | [Identificador](identifier.md) | S   | N        |
| Recurso\_ | [Identificador](identifier.md) | N   | N        |
| Ação    | [Identificador](identifier.md) | N   | S        |
| Ordenando  | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Billboard"></span><span id="billboard"></span><span id="BILLBOARD"></span>Mensagem
</dt> <dd>

Nome do [controle do mural](billboard-control.md).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_
</dt> <dd>

Uma chave externa para a primeira coluna da [tabela de recursos](feature-table.md). O mural será exibido somente se esse recurso estiver sendo instalado.

</dd> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action
</dt> <dd>

O nome de uma ação. O mural é exibido durante as mensagens de andamento recebidas desta ação.

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordenação
</dt> <dd>

Se houver mais de um mural correspondente a uma ação, eles serão exibidos na ordem definida por esta coluna. Esse número deve ser não negativo.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE95](ice95.md)  
</dl>

 

 



