---
description: ICE88 valida que o diretório referenciado na coluna DirProperty da tabela IniFile existe no pacote Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829673"
---
# <a name="ice88"></a>ICE88

ICE88 valida que o diretório referenciado na coluna DirProperty da [tabela inifile](inifile-table.md) existe no pacote Windows Installer. ICE88 emitirá um aviso se o valor de DirProperty não representar uma propriedade nas tabelas Directory, AppSearch ou Property, determinadas [Propriedades de pasta do sistema](property-reference.md)ou uma propriedade definida por uma ação personalizada Type 51.

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



| Aviso de ICE88                                                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Na entrada da tabela IniFile (IniFile =) \[ 3 \] , DirProperty = \[ 1 \] não é encontrado nas tabelas Directory/Property/AppSearch/CA-Type51 e não é uma das propriedades do instalador. | Para cada registro na tabela IniFile, ICE88 lê o valor na coluna DirProperty. ICE88 verifica o valor na tabela de [diretórios](directory-table.md), na tabela [AppSearch](appsearch-table.md)e na [tabela de propriedades](property-table.md) e também examina a lista de propriedades definidas pelo instalador. ICE88 lança esse aviso se o valor não puder ser encontrado na verificação. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



