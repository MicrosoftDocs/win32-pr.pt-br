---
description: O tipo de identificador do tipo semântico é um dos tipos de formato de texto.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091537"
---
# <a name="identifier-type"></a>Tipo de identificador

O tipo de identificador do [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md). Esse tipo consiste em uma cadeia de caracteres de texto fornecida pelo usuário no formato de um [identificador](identifier.md)de Windows Installer. A ferramenta de mesclagem substitui essa cadeia de caracteres nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna formato, inserir "identificador" na coluna tipo e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres pode estar em qualquer idioma compatível com a página de código do banco de dados. Consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md). NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.

 

 



