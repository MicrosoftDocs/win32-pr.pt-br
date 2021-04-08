---
description: O tipo formatado de tipo semântico é um dos tipos de formato de texto.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo formatado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010706"
---
# <a name="formatted-type"></a>Tipo formatado

O tipo formatado de [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md). Esse tipo consiste em uma cadeia de caracteres de texto arbitrária de qualquer comprimento fornecido pelo usuário e no Windows Installer formato de texto formatado. Para obter detalhes, consulte [formatado](formatted.md). A ferramenta de mesclagem substitui essa cadeia de caracteres nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna formato, inserir "formatado" na coluna tipo e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres pode estar em qualquer idioma compatível com a página de código do banco de dados. Para obter detalhes, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md). NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.

 

 



