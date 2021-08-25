---
title: Como Ferramentas para Desenvolvedores usar bibliotecas de tipos
description: Como Ferramentas para Desenvolvedores usar bibliotecas de tipos
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e829459176d96beab3fd818b7bafe3cddfb7969ff46531d26709ef6391ecc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993066"
---
# <a name="how-developer-tools-use-type-libraries"></a>Como Ferramentas para Desenvolvedores usar bibliotecas de tipos

O diagrama a seguir ilustra como as várias ferramentas de desenvolvimento interagem com uma biblioteca de tipos do objeto COM. Cada biblioteca de tipos expõe as interfaces padrão programáticas que as ferramentas podem chamar para obter informações sobre os elementos descritos nessa biblioteca de tipos. Neste diagrama, GUID significa identificador global exclusivo e RPC para chamada de procedimento remoto.

![Diagrama que mostra como a ferramenta de desenvolvimento interage com uma biblioteca de tipos do objeto C O M.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

no diagrama anterior, as ferramentas de conversão de C++, como o compilador MIDL e os assistentes fornecidos pelo sistema de desenvolvimento de Microsoft Visual C++, geram arquivos de cabeçalho e stub. Você pode adicionar esses arquivos ao seu projeto para usar o objeto COM descrito pela biblioteca de tipos.

Da mesma forma, em Java, as ferramentas de desenvolvedor geram arquivos de classe e origem Java, que podem ser importados em seu aplicativo.

em Visual Basic, o cenário é um pouco mais simples. Você não precisa gerar arquivos adicionais. o ambiente de Visual Basic fornece caixas de diálogo que listam os objetos COM atualmente instalados no computador. Você seleciona o componente que deseja chamar do seu aplicativo e ele é adicionado ao seu projeto, seja como um componente ou uma referência.

O visualizador OLE-COM lê uma biblioteca de tipos, gera um arquivo IDL temporário com base na biblioteca de tipos e exibe-o para os usuários. O visualizador OLE-COM também exibe a sintaxe C++ para os elementos COM listados na biblioteca de tipos.

Para obter mais informações sobre bibliotecas de tipos, consulte [bibliotecas de tipos e a linguagem de descrição de objeto](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).

 

 