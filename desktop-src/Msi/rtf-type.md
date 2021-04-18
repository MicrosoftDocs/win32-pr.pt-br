---
description: O tipo de tipo de semântica RTF é um dos tipos de formato de texto.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Tipo RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81c708183596d794f20e38bf89c073472e3affb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750220"
---
# <a name="rtf-type"></a>Tipo RTF

O tipo de [tipo de semântica](semantic-types.md) RTF é um dos [tipos de formato de texto](text-format-types.md). Esse tipo consiste em uma cadeia de caracteres de texto arbitrária no RTF (Rich Text Format) de qualquer comprimento fornecido pelo usuário. A ferramenta de mesclagem substitui essa cadeia de caracteres nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna formato, inserir "RTF" na coluna tipo e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres pode estar em qualquer idioma compatível com a página de código do banco de dados. Consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md). NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.

 

 



