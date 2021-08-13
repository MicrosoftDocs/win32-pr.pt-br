---
description: A ação RemoveIniValues remove .ini de arquivo especificadas para remoção na tabela RemoveIniFile se o componente estiver definido para ser instalado localmente ou run-from-source.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Ação RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095985165bf6d9629aa0cae67a5b3f7975d817151ac4b04de40a08d5c2bab4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626385"
---
# <a name="removeinivalues-action"></a>Ação RemoveIniValues

A ação RemoveIniValues remove .ini de arquivo especificadas para remoção na tabela [RemoveIniFile](removeinifile-table.md) se o componente estiver definido para ser instalado localmente ou run-from-source. A ação RemoveIniValues remove .ini informações de arquivo que foram associadas a um componente na [tabela IniFile](inifile-table.md). Essa ação também removerá .ini de arquivo se as informações foram escritas pela ação [WriteIniValues](writeinivalues-action.md) e o componente estiver agendado para ser desinstalado.

## <a name="sequence-restrictions"></a>Restrições de sequência

A [ação InstallValidate](installvalidate-action.md) deve ser chamada antes da ação RemoveIniValues. Se uma [ação WriteIniValues](writeinivalues-action.md) for usada na sequência, ela deverá aparecer após RemoveIniValues.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação    |
|-------|-------------------------------|
| \[1\] | Identificador do .ini arquivo.      |
| \[2\] | Uma .ini chave de arquivo.     |
| \[3\] | Item removido do .ini arquivo.  |
| \[4\] | Valor removido do .ini arquivo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela RemoveIniFile](removeinifile-table.md)
</dt> <dt>

[Tabela IniFile](inifile-table.md)
</dt> <dt>

[Ação WriteIniValues](writeinivalues-action.md)
</dt> <dt>

[InstallValidate](installvalidate-action.md)
</dt> </dl>

 

 



