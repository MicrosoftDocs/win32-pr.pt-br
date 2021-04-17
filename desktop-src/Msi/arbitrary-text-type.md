---
description: O tipo de texto arbitrário do tipo semântico é um dos tipos de formato de texto.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo de texto arbitrário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750823"
---
# <a name="arbitrary-text-type"></a>Tipo de texto arbitrário

O tipo de texto arbitrário do [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md). Esse tipo consiste em uma cadeia de caracteres de texto arbitrária de qualquer comprimento fornecido pelo usuário. A ferramenta de mesclagem substitui essa cadeia de caracteres arbitrária nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna de formato e deixar em branco as colunas Type e ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres de texto arbitrário pode estar em qualquer idioma compatível com a página de código do banco de dados. Para obter detalhes, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md). NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.

 

 



