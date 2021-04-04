---
description: A ação WriteIniValues grava as informações do arquivo. ini que o aplicativo precisa gravar em seus arquivos. ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Ação WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828854"
---
# <a name="writeinivalues-action"></a>Ação WriteIniValues

A ação WriteIniValues grava as informações do arquivo. ini que o aplicativo precisa gravar em seus arquivos. ini. A gravação dessas informações é restringida pela tabela de [componentes](component-table.md). Um valor. ini será gravado se o componente correspondente tiver sido configurado para ser instalado localmente ou executado a partir da origem.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallValidate deve vir antes da ação WriteIniValues. Se houver uma [ação RemoveIniValues](removeinivalues-action.md) na sequência, ela deverá vir antes da ação WriteIniValues.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação              |
|-------|-----------------------------------------|
| \[1\] | Identificador do arquivo. ini.                |
| \[2\] | a chave de arquivo. ini na seção a seguir. |
| \[3\] | Item removido do arquivo. ini.            |
| \[4\] | Valor removido do arquivo. ini.           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela IniFile](inifile-table.md)
</dt> </dl>

 

 



