---
description: A ação WriteIniValues grava as .ini de arquivo que o aplicativo precisa gravar em seus .ini arquivos.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Ação WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2551725e7b12a697e35b08b403011044bbd631b3ff5bf3d0a5923ecb4c99e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942094"
---
# <a name="writeinivalues-action"></a>Ação WriteIniValues

A ação WriteIniValues grava as .ini de arquivo que o aplicativo precisa gravar em seus .ini arquivos. A escrita dessas informações é controlada pela [tabela Componente](component-table.md). Um .ini valor será gravado se o componente correspondente tiver sido definido para ser instalado localmente ou executado da origem.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallValidate deve vir antes da ação WriteIniValues. Se houver uma ação [RemoveIniValues](removeinivalues-action.md) na sequência, ela deverá vir antes da ação WriteIniValues.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação              |
|-------|-----------------------------------------|
| \[1\] | Identificador do .ini arquivo.                |
| \[2\] | .ini de arquivo na seção a seguir. |
| \[3\] | Item removido do .ini arquivo.            |
| \[4\] | Valor removido do .ini arquivo.           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tabela IniFile](inifile-table.md)
</dt> </dl>

 

 



