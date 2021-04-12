---
description: O tipo de inteiro arbitrário do tipo semântico é um dos tipos de formato inteiro.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Tipo de inteiro arbitrário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091543"
---
# <a name="arbitrary-integer-type"></a>Tipo de inteiro arbitrário

O tipo de inteiro arbitrário do [tipo semântico](semantic-types.md) é um dos [tipos de formato inteiro](integer-format-types.md). Esse tipo de item configurável é um inteiro fornecido pelo usuário. A ferramenta de mesclagem substitui esse inteiro nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md).

Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome da cadeia de texto na coluna nome, inserir "2" na coluna formato e deixar em branco as colunas Type e ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md). As colunas Type e ContextData são reservadas e devem ser nulas.

 

 



