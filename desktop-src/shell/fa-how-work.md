---
description: As associações de arquivo definem como o Shell trata um tipo de arquivo no sistema.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Como funcionam as associações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169449"
---
# <a name="how-file-associations-work"></a>Como funcionam as associações de arquivo

As associações de arquivo definem como o Shell trata um [tipo de arquivo](fa-file-types.md) no sistema.

Este tópico é organizado da seguinte maneira:

-   [Sobre associações de arquivo](#about-file-associations)
-   [Quando você deve implementar ou modificar associações de arquivo](#when-you-should-implement-or-modify-file-associations)
-   [Como funcionam as associações de arquivo](#how-file-associations-work)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="about-file-associations"></a>Sobre associações de arquivo

As associações de arquivo controlam a seguinte funcionalidade:

-   Qual aplicativo é iniciado quando um usuário clica duas vezes em um arquivo.
-   Qual ícone aparece para um arquivo por padrão.
-   Como o tipo de arquivo aparece quando exibido no Windows Explorer.
-   Quais comandos aparecem no menu de atalho de um arquivo.
-   Outros recursos de interface do usuário, como dicas de ferramenta, informações de bloco e o painel detalhes.

Os desenvolvedores de aplicativos podem usar associações de arquivos para controlar como o Shell trata tipos de arquivo personalizados ou para associar um aplicativo a tipos de arquivo existentes. Por exemplo, quando um aplicativo é instalado, o aplicativo pode verificar a presença de associações de arquivo existentes e criar ou substituir essas associações de arquivo.

Os usuários podem controlar alguns aspectos das associações de arquivo para personalizar como o Shell trata um tipo de arquivo usando a interface do usuário **abrir com** ou editando o registro.

Na janela do Windows Explorer mostrada na captura de tela abaixo, o Shell exibe ícones diferentes para cada arquivo, com base no ícone associado ao tipo de arquivo. Se o usuário clicar duas vezes na **imagem de bitmap de exemplo** de arquivo, o Shell iniciará o Paint e o usará para abrir o arquivo porque, nesse sistema, o Paint será associado a arquivos. bmp. As pessoas podem controlar essas ações usando associações de arquivos.

![ilustração de como as associações de arquivo funcionam na prática](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>Quando você deve implementar ou modificar associações de arquivo

Os aplicativos podem usar arquivos para várias finalidades: alguns arquivos são usados exclusivamente pelo aplicativo e, normalmente, não são acessados por usuários, enquanto outros arquivos são criados pelo usuário e são frequentemente abertos, pesquisados e exibidos no Shell.

A menos que o tipo de arquivo personalizado seja usado exclusivamente pelo aplicativo, você deve implementar associações de arquivo para ele. Como regra geral, implemente as associações de arquivo para o tipo de arquivo personalizado se você espera que o usuário interaja diretamente com esses arquivos de qualquer forma. Isso inclui o uso do Shell para procurar e abrir os arquivos, pesquisar o conteúdo ou as propriedades dos arquivos e visualizar os arquivos.

Se seu aplicativo estiver manipulando um tipo de arquivo existente, não modifique a associação de arquivo, a menos que você queira modificar a maneira como o Shell manipula todos os arquivos desse tipo.

## <a name="how-file-associations-work"></a>Como funcionam as associações de arquivo

Os arquivos são expostos no Shell como itens de Shell. Para controlar as associações de arquivos, os desenvolvedores de aplicativos podem registrar um mapeamento entre o tipo de arquivo e os manipuladores (objetos COM que fornecem funcionalidade para os itens de shell do tipo de arquivo). Quando o Shell precisa consultar as associações de arquivo de um tipo de arquivo, ele cria uma matriz de chaves do registro contendo as associações para o tipo de arquivo e verifica essas chaves para que as associações de arquivo apropriadas sejam usadas.

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter um plano de fundo conceitual sobre associações de arquivo, consulte [visão geral de verbos e associações de arquivo](fa-verbs.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[registro de Aplicativo](app-registration.md)
</dt> <dt>

[Tipos de arquivo](fa-file-types.md)
</dt> <dt>

[Exibição de conteúdo por tipo de arquivo ou tipo](prophand-content-view.md)
</dt> <dt>

[Verificador de tipo de arquivo](file-type-verifier.md)
</dt> <dt>

[Manipuladores de tipo de arquivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores programáticos](fa-progids.md)
</dt> <dt>

[Tipos observados](fa-perceivedtypes.md)
</dt> <dt>

[Matrizes de associação](fa-associationarray.md)
</dt> </dl>

 

 



