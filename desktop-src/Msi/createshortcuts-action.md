---
description: A ação createshortcuts gerencia a criação de atalhos.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Ação createatalhos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011602"
---
# <a name="createshortcuts-action"></a>Ação createatalhos

A ação createshortcuts gerencia a criação de atalhos.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação createshortcuts deve vir após a ação [InstallFiles](installfiles-action.md) e a ação [RemoveShortcuts](removeshortcuts-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação      |
|-------|---------------------------------|
| \[1\] | Identificador do atalho criado. |



 

## <a name="remarks"></a>Comentários

A ação createshortcuts cria atalhos para os principais arquivos de componentes dos recursos selecionados para instalação ou anúncio.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela de atalho](shortcut-table.md)
</dt> <dt>

[Tabela MsiShortcutProperty](msishortcutproperty-table.md)
</dt> </dl>

 

 



