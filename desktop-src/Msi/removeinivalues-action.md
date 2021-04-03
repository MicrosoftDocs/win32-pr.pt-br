---
description: A ação RemoveIniValues remove as informações do arquivo. ini especificadas para remoção na tabela RemoveIniFile se o componente estiver configurado para ser instalado localmente ou executado de origem.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Ação RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922738"
---
# <a name="removeinivalues-action"></a>Ação RemoveIniValues

A ação RemoveIniValues remove as informações do arquivo. ini especificadas para remoção na [tabela RemoveIniFile](removeinifile-table.md) se o componente estiver configurado para ser instalado localmente ou executado de origem. A ação RemoveIniValues remove informações do arquivo. ini que foram associadas a um componente na [tabela inifile](inifile-table.md). Essa ação também removerá informações do arquivo. ini se as informações tiverem sido gravadas pela [ação WriteIniValues](writeinivalues-action.md) e o componente estiver agendado para ser desinstalado.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação [InstallValidate](installvalidate-action.md) deve ser chamada antes da ação RemoveIniValues. Se uma ação [WriteIniValues](writeinivalues-action.md) for usada na sequência, ela deverá aparecer após RemoveIniValues.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação    |
|-------|-------------------------------|
| \[1\] | Identificador do arquivo. ini.      |
| \[2\] | Uma seção de chave de arquivo. ini.     |
| \[3\] | Item removido do arquivo. ini.  |
| \[4\] | Valor removido do arquivo. ini. |



 

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

 

 



