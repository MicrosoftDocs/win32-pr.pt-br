---
description: O Verificador de Tipo de Arquivo é uma ferramenta que permite que isVs (fornecedores independentes de software) verifiquem se seus tipos de arquivo exclusivos são implementados corretamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Verificador de Tipo de Arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad3d3e66d85413a209c6899ce16061fa1fd46468fa32462026485d49b7326dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009506"
---
# <a name="file-type-verifier"></a>Verificador de Tipo de Arquivo

O Verificador de Tipo de Arquivo é uma ferramenta que permite que isVs (fornecedores independentes de software) verifiquem se seus tipos de arquivo exclusivos são implementados corretamente. Implementações de alta qualidade de seus manipuladores de tipo de arquivo são cruciais para uma boa experiência do usuário, pois os usuários interagem com o formato de arquivo de várias maneiras no Windows Explorer. Os usuários podem fazer pesquisas de texto completo, classificar por metadados personalizados ou exibir miniaturas e visualizações rich do formato de arquivo.

Para obter instruções sobre como usar o Verificador de Tipo de Arquivo, [consulte How To Use the File Type Verifier](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>Sobre a ferramenta verificador de tipo de arquivo

O Verificador de Tipo de Arquivo é um programa que está disponível como parte do [SDK Windows 7.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Ele foi projetado para ajudar os desenvolvedores que criam tipos Windows [arquivos](fa-file-types.md) personalizados para detectar possíveis problemas com seus tipos de arquivo. Embora o Verificador de Tipo de Arquivo seja executado somente no Windows 7 e posterior, as regras que o Verificador de Tipo de Arquivo impõe se aplicam a todas as versões do Windows em que os recursos verificados estão disponíveis.

O Verificador de Tipo de Arquivo executa vários testes no tipo de arquivo para verificar se ele está registrado corretamente e se ele fornece os Manipuladores de Tipo de Arquivo [apropriados](fa-file-extensions.md) para exibir o tipo de arquivo corretamente no Gerenciador do Windows e, quando apropriado, que ele dá suporte à indexação do conteúdo do arquivo.

O Verificador de Tipo de Arquivo testa as seguintes coisas:

-   [Manipuladores de visualização](building-preview-handlers.md)
-   [Manipuladores de miniaturas](building-thumbnail-providers.md)
-   [Manipuladores de propriedades](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Manipuladores de verbos](fa-verbs.md)
-   [Filtros (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Associações de tipos](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Tipos percebidos](fa-perceivedtypes.md)
-   [Propriedades importantes](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como usar o verificador de tipo de arquivo](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[Registro de aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Como funcionam as associações de arquivos](fa-how-work.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos percebidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 
