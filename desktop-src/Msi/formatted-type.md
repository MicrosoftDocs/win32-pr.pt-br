---
description: O tipo formatado de tipo semântico é um dos tipos de formato de texto.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo formatado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09fc535a48f6d2e89cc46fb0d64ee998b8c062d6c2a406b9d5b8801ef1b62293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044326"
---
# <a name="formatted-type"></a>Tipo formatado

O tipo formatado de [tipo semântico](semantic-types.md) é um dos [tipos de formato de texto](text-format-types.md). esse tipo consiste em uma cadeia de caracteres de texto arbitrária de qualquer comprimento fornecido pelo usuário e no Windows Installer formato de texto formatado. Para obter detalhes, consulte [formatado](formatted.md). A ferramenta de mesclagem substitui essa cadeia de caracteres nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "0" na coluna formato, inserir "formatado" na coluna tipo e deixar em branco a coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres pode estar em qualquer idioma compatível com a página de código do banco de dados. para obter detalhes, consulte [manipulação de página de código (Windows Installer)](code-page-handling-windows-installer-.md). NULL é um valor válido para a cadeia de caracteres de texto, a menos que o msmConfigItemNonNullable tenha sido incluído no campo atributos da Tabela ModuleConfiguration.

 

 



