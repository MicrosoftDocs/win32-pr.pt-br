---
description: O código do pacote do pacote de atualização deve ser alterado do produto original.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Atualizando informações de resumo para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9bee3457b9ebbe0264d569f37d8ed5a3e372df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011717"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Atualizando informações de resumo para uma atualização

O código do pacote do pacote de atualização deve ser alterado do produto original. O código do pacote é armazenado na propriedade [**Summary do número de revisão**](revision-number-summary.md) . Para obter detalhes, consulte [códigos de pacote](package-codes.md). Use Msiinfo.exe, ou outro editor, para alterar as informações de Resumo de MNP2001.msi conforme descrito em [adicionando informações de resumo](adding-summary-information.md).



| Propriedade de informações de resumo                                                   | Dados                                                                             | Observações                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modelo**](template-summary.md)(plataforma e idioma)<br/>         | ; 1033                                                                            | Plataforma e idioma usados pelo banco de dados. Se a especificação da plataforma estiver ausente no valor da propriedade de resumo do [**modelo**](template-summary.md) , o instalador assumirá a arquitetura Intel. A propriedade [**ProductLanguage**](productlanguage.md) do banco de dados é normalmente usada para essa propriedade de resumo. A ID de idioma do exemplo indica que o pacote usa inglês americano. |
| [**Número de revisão**](revision-number-summary.md)(código do pacote)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | Este é o [GUID](guid.md) de código do pacote que identifica exclusivamente o pacote de exemplo. Se você reproduzir esse exemplo, use um utilitário como GUIDGEN para gerar um GUID diferente para seu pacote. Os resultados de GUIDGEN contêm caracteres minúsculos, observe que você deve alterar todos os caracteres minúsculos para letras maiúsculas para um código de pacote válido.                                                     |
| [**Contagem de páginas**](page-count-summary.md)(versão mínima do instalador)<br/> | 200                                                                              | Para um mínimo de Windows Installer versão 2,0, essa propriedade deve ser definida como o inteiro 200.                                                                                                                                                                                                                                                                                                         |
| [**Contagem de palavras**](word-count-summary.md)(tipo de origem)<br/>            | 0                                                                                | O tipo de origem global para o pacote são nomes de arquivo longos e não compactados. Para obter mais informações, consulte [fontes compactadas e descompactadas](compressed-and-uncompressed-sources.md) e a descrição da coluna atributos da [tabela de arquivos](file-table.md).                                                                                                                               |
| [**Título**](title-summary.md)                                                 | Banco de dados de instalação                                                            | Informa aos usuários que esse banco de dados destina-se a uma instalação em vez de uma transformação ou um patch.                                                                                                                                                                                                                                                                                                          |
| [**Assunto**](subject-summary.md)                                             | MNP2001                                                                          | Os navegadores de arquivos podem exibir isso como o produto a ser instalado com esse banco de dados.                                                                                                                                                                                                                                                                                                                    |
| [**Palavras-chave**](keywords-summary.md)                                           | Instalador, MSI, banco de dados                                                         | Navegadores de arquivos com capacidade de pesquisa de palavra-chave podem pesquisar essas palavras.                                                                                                                                                                                                                                                                                                                      |
| [**Autor**](author-summary.md)                                               | Microsoft Corporation                                                            | Nome do fabricante do produto.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Comentários**](comments-summary.md)                                           | Este banco de dados do instalador contém a lógica e os requisitos necessários para instalar o bloco de notas. | Informa os usuários sobre a finalidade deste banco de dados.                                                                                                                                                                                                                                                                                                                                                    |
| [**Criando aplicativo**](creating-application-summary.md)                   | Orca                                                                             | Aplicativo usado para criar o banco de dados de instalação. O exemplo especifica o editor de banco de dados Orca como um exemplo.                                                                                                                                                                                                                                                                                   |
| [**Segurança**](security-summary.md)                                           | 0                                                                                | O banco de dados de exemplo é de leitura/gravação irrestrita.                                                                                                                                                                                                                                                                                                                                                      |



 

[Continuar](validating-an-installation-upgrade.md)

 

 




