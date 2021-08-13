---
description: A ação RemoveRegistryValues só pode remover valores do registro do sistema que foram autorados na tabela registro ou na tabela RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Ação RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fe284043f76cbffe3fe6a6887f46d6ab16ba65e9103efce6e4e62baac31d31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339656"
---
# <a name="removeregistryvalues-action"></a>Ação RemoveRegistryValues

A ação RemoveRegistryValues só pode remover valores do registro do [](registry-table.md) sistema que foram autorados na tabela registro ou na [tabela RemoveRegistry](removeregistry-table.md). Essa ação remove um valor do Registro que foi criado na tabela do Registro se o componente associado foi instalado localmente ou como executado da origem e agora está definido para ser desinstalado. Essa ação removerá um valor do Registro que foi criado na tabela RemoveRegistry se o componente associado estiver definido para ser instalado localmente ou como executado da origem.

## <a name="sequence-restrictions"></a>Restrições de sequência

A [ação InstallValidate](installvalidate-action.md) deve ser chamada antes de chamar RemoveRegistryValues. Se uma [ação WriteRegistryValues](writeregistryvalues-action.md) for usada, ela deverá vir após RemoveRegistryValues. RemoveRegistryValues deve vir [antes de UnregisterMIMEInfo](unregistermimeinfo-action.md) ou [UnregisterProgIDInfo](unregisterprogidinfo-action.md).

Uma ação personalizada pode ser usada [](registry-table.md) para adicionar linhas à tabela do Registro durante uma instalação, desinstalação ou transação de reparo. Essas linhas não persistem na tabela registro e as informações só estão disponíveis durante a transação atual. Portanto, a ação personalizada deve ser executado em cada instalação, desinstalação ou transação de reparo que exija as informações nessas linhas adicionais. A ação personalizada deve vir antes das ações RemoveRegistryValues [e WriteRegistryValues](writeregistryvalues-action.md) na sequência de ação.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                          |
|-------|-----------------------------------------------------|
| \[1\] | Caminho do Registro para a chave do valor do Registro removido.     |
| \[2\] | Cadeia de caracteres formatada de nome do valor do Registro removido. |



 

## <a name="remarks"></a>Comentários

Para remover um valor do Registro, registre o valor na coluna Valor da tabela Registro. Se a ação WriteRegistryValues tiver anexado cadeias de caracteres REG MULTI SZ ao valor na tabela do Registro , a ação \_ \_ RemoveRegistryValues [](registry-table.md)removerá apenas essas cadeias de caracteres do valor do Registro.

 

 



