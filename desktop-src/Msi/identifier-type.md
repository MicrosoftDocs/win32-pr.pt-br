---
description: O Tipo de Identificador do tipo semântico é um dos Tipos de Formato de Texto.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1061f6d813b0803dbe1aa0d8e49e7f93cffba6e100f778901441f4bc4ed710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634777"
---
# <a name="identifier-type"></a>Tipo de identificador

O Tipo de Identificador do [tipo semântico](semantic-types.md) é um dos Tipos [de Formato de Texto](text-format-types.md). Esse tipo consiste em uma cadeia de caracteres de texto fornecida pelo usuário no formato de um identificador Windows [instalador.](identifier.md) A ferramenta de mesclagem substitui essa cadeia de caracteres nos modelos especificados na coluna Valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de caracteres de texto na coluna Nome, inserir "0" na coluna Formato, inserir "Identificador" na coluna Tipo e deixar em branco a coluna ContextData da tabela [ModuleConfiguration](moduleconfiguration-table.md). A cadeia de caracteres pode estar em qualquer linguagem compatível com a página de código do banco de dados. Consulte [Tratamento de página de código (Windows Instalador)](code-page-handling-windows-installer-.md). Null é um valor válido para a cadeia de caracteres de texto, a menos que msmConfigItemNonNullable tenha sido incluído no campo Atributos da tabela ModuleConfiguration.

 

 



