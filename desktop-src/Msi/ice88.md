---
description: ICE88 valida que o diretório referenciado na coluna DirProperty da tabela IniFile existe no pacote Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cb49ce6cb4363cfe89879f6e72b7ce801c063ea2b278c03dacf5cbadacddce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105216"
---
# <a name="ice88"></a>ICE88

ICE88 valida que o diretório referenciado na coluna DirProperty da [tabela IniFile](inifile-table.md) existe no pacote Windows Installer. ICE88 emitirá um aviso se o valor de DirProperty não representar uma propriedade nas tabelas Directory, AppSearch ou Property, determinadas [Propriedades de pasta do sistema](property-reference.md)ou uma propriedade definida por uma ação personalizada Type 51.

O ICE88 examina as tabelas e propriedades a seguir.

-   [Tabela de diretórios](directory-table.md)
-   [Tabela AppSearch](appsearch-table.md)
-   [Tabela de propriedades](property-table.md)
-   [Tabela CustomAction](customaction-table.md) , em que a ação personalizada é um [tipo de ação personalizada 51](custom-action-type-51.md)
-   [**Propriedade ProgramFilesFolder**](programfilesfolder.md)
-   [**Propriedade CommonFilesFolder**](commonfilesfolder.md)
-   [**Propriedade SystemFolder**](systemfolder.md)
-   [**Propriedade ProgramFiles64Folder**](programfiles64folder.md)
-   [**Propriedade CommonFiles64Folder**](commonfiles64folder.md)
-   [**Propriedade System64Folder**](system64folder.md)

## <a name="result"></a>Resultado

ICE88 posta o aviso a seguir.



| Aviso de ICE88                                                                                                                                                                  | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Na entrada da tabela IniFile (IniFile =) \[ 3 \] , DirProperty = \[ 1 \] não é encontrado nas tabelas Directory/Property/AppSearch/CA-Type51 e não é uma das propriedades do instalador. | Para cada registro na tabela IniFile, ICE88 lê o valor na coluna DirProperty. ICE88 verifica o valor na tabela de [diretórios](directory-table.md), na tabela [AppSearch](appsearch-table.md)e na [tabela de propriedades](property-table.md) e também examina a lista de propriedades definidas pelo instalador. ICE88 lança esse aviso se o valor não puder ser encontrado na verificação. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



