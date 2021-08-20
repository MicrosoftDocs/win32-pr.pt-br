---
description: O código do pacote de atualização deve ser alterado do produto original.
ms.assetid: 786e864a-93e0-4ea6-adab-e87afbdd6ac2
title: Atualizando informações de resumo para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6849a315f5251538acc749d3c3a2ed5605d82ec4159fadf584b5a087a9beaeee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141592"
---
# <a name="updating-summary-information-for-an-upgrade"></a>Atualizando informações de resumo para uma atualização

O código do pacote de atualização deve ser alterado do produto original. O código do pacote é armazenado na propriedade [**Resumo do Número de**](revision-number-summary.md) Revisão. Para obter detalhes, consulte [Códigos de pacote](package-codes.md). Use Msiinfo.exe, ou outro editor, para alterar as informações resumidas do MNP2001.msi conforme descrito em [Adicionando informações resumidas.](adding-summary-information.md)



| Propriedade de informações de resumo                                                   | Dados                                                                             | Observações                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modelo**](template-summary.md)(plataforma e linguagem)<br/>         | ;1033                                                                            | Plataforma e idioma usados pelo banco de dados. Se a especificação da plataforma estiver ausente no valor da propriedade [**Resumo**](template-summary.md) do Modelo, o instalador assumirá a arquitetura da Intel. A [**propriedade ProductLanguage**](productlanguage.md) do banco de dados normalmente é usada para essa propriedade de resumo. A ID de idioma do exemplo indica que o pacote usa o inglês dos EUA. |
| [**Número de revisão**](revision-number-summary.md)(código do pacote)<br/>    | {A0EC5348-1D02-4FF6-93F5-61BD7AC1772E}                                           | Esse é o GUID do código [do](guid.md) pacote que identifica exclusivamente o pacote de exemplo. Se você reproduzir este exemplo, use um utilitário como GUIDGEN para gerar um GUID diferente para seu pacote. Os resultados de GUIDGEN contêm caracteres minúsculos, observe que você deve alterar todos os caracteres minúsculos para maiúsculas para um código de pacote válido.                                                     |
| [**Contagem de páginas**](page-count-summary.md)(versão mínima do instalador)<br/> | 200                                                                              | Para uma versão Windows Installer versão 2.0, essa propriedade deve ser definida como o inteiro 200.                                                                                                                                                                                                                                                                                                         |
| [**Contagem de palavras**](word-count-summary.md)(tipo de origem)<br/>            | 0                                                                                | O tipo de origem global para o pacote são nomes de arquivo longos e descompactados. Para obter mais informações, consulte Fontes compactadas e [descompactados](compressed-and-uncompressed-sources.md) e a descrição da coluna Atributos da [tabela Arquivo](file-table.md).                                                                                                                               |
| [**Título**](title-summary.md)                                                 | Banco de dados de instalação                                                            | Informa aos usuários que esse banco de dados é para uma instalação em vez de uma transformação ou um patch.                                                                                                                                                                                                                                                                                                          |
| [**Assunto**](subject-summary.md)                                             | MNP2001                                                                          | Os navegadores de arquivos podem exibir isso como o produto a ser instalado com esse banco de dados.                                                                                                                                                                                                                                                                                                                    |
| [**Palavras-chave**](keywords-summary.md)                                           | Instalador, MSI, Banco de Dados                                                         | Navegadores de arquivos que são capazes de pesquisar palavras-chave podem pesquisar essas palavras.                                                                                                                                                                                                                                                                                                                      |
| [**Autor**](author-summary.md)                                               | Microsoft Corporation                                                            | Nome do fabricante do produto.                                                                                                                                                                                                                                                                                                                                                                  |
| [**Comentários**](comments-summary.md)                                           | Esse banco de dados do instalador contém a lógica e os dados necessários para instalar Bloco de notas. | Informa os usuários sobre a finalidade desse banco de dados.                                                                                                                                                                                                                                                                                                                                                    |
| [**Criando aplicativo**](creating-application-summary.md)                   | Orca                                                                             | Aplicativo usado para criar o banco de dados de instalação. O exemplo especifica o editor de banco de dados Orca como um exemplo.                                                                                                                                                                                                                                                                                   |
| [**Segurança**](security-summary.md)                                           | 0                                                                                | O banco de dados de exemplo é leitura/gravação irrestrita.                                                                                                                                                                                                                                                                                                                                                      |



 

[Continuar](validating-an-installation-upgrade.md)

 

 




