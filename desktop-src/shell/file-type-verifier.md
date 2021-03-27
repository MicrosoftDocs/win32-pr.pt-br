---
description: O verificador de tipo de arquivo é uma ferramenta que permite que fornecedores de software independentes (ISVs) verifiquem se seus tipos de arquivo exclusivos são implementados corretamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Verificador de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828304"
---
# <a name="file-type-verifier"></a>Verificador de tipo de arquivo

O verificador de tipo de arquivo é uma ferramenta que permite que fornecedores de software independentes (ISVs) verifiquem se seus tipos de arquivo exclusivos são implementados corretamente. Implementações de alta qualidade dos manipuladores de tipo de arquivo são cruciais para uma boa experiência de usuário, pois os usuários interagem com o formato de arquivo de várias maneiras no Windows Explorer. Os usuários podem fazer pesquisas de texto completo, classificar por metadados personalizados ou exibir miniaturas e visualizações ricas de seu formato de arquivo.

Para obter instruções sobre como usar o verificador de tipo de arquivo, consulte [como usar o verificador de tipo de arquivo](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>Sobre a ferramenta de verificação de tipo de arquivo

O File Type Verifier é um programa que está disponível como parte do [SDK do Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Ele foi projetado para ajudar os desenvolvedores que criam [tipos de arquivos](fa-file-types.md) personalizados do Windows a detectarem possíveis problemas com seus tipos de arquivo. Embora o verificador de tipo de arquivo seja executado somente no Windows 7 e posterior, as regras que o verificador de tipo de arquivo impõe aplicam-se a todas as versões do Windows onde os recursos que ele verifica estão disponíveis.

O verificador de tipo de arquivo executa vários testes no tipo de arquivo para verificar se ele está registrado corretamente e se ele fornece os [manipuladores de tipo de arquivo](fa-file-extensions.md) apropriados para exibir o tipo de arquivo corretamente no Windows Explorer e, quando apropriado, que ele dá suporte à indexação do conteúdo do arquivo.

O verificador de tipo de arquivo testa as seguintes coisas:

-   [Gerenciadores de visualização](building-preview-handlers.md)
-   [Manipuladores de miniatura](building-thumbnail-providers.md)
-   [Manipuladores de propriedade](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Manipuladores de verbo](fa-verbs.md)
-   [Filtros (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Associações de tipo](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Tipos observados](fa-perceivedtypes.md)
-   [Propriedades importantes](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o verificador de tipo de arquivo](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[registro de Aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivo](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos observados](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 
