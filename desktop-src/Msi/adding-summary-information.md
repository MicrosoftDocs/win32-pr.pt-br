---
description: As propriedades de Resumo de informações a seguir devem ser definidas em todos os pacotes de instalação, usando uma ferramenta de software para acessar a interface IStream do fluxo de informações de resumo.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Adicionando informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26486e0082a05b05fbdc9609881083e10cddb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091547"
---
# <a name="adding-summary-information"></a>Adicionando informações de resumo

As propriedades de Resumo de informações a seguir devem ser definidas em todos os pacotes de instalação, usando uma ferramenta de software para acessar a interface **IStream** do [fluxo de informações de resumo](summary-information-stream.md). Por exemplo, você pode usar a ferramenta Msiinfo.exe fornecida com o SDK do Windows Installer para definir essas propriedades. Se essas propriedades não forem definidas, o pacote não passará na [validação do pacote](package-validation.md).



| Propriedade de informações de resumo                                                   | Dados                                   | Observações                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modelo**](template-summary.md)(plataforma e idioma)<br/>         | ; 1033                                  | Plataforma e idioma usados pelo banco de dados. Se a especificação da plataforma estiver ausente no valor da propriedade de resumo do [**modelo**](template-summary.md) , o instalador assumirá a arquitetura Intel. A propriedade [**ProductLanguage**](productlanguage.md) do banco de dados é normalmente usada para essa propriedade de resumo. A ID de idioma do exemplo indica que o pacote usa inglês americano. |
| [**Número de revisão**](revision-number-summary.md)(código do pacote)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | Este é o [GUID](guid.md) de código do pacote que identifica exclusivamente o pacote de exemplo. Se você reproduzir esse exemplo, use um utilitário como GUIDGEN para gerar um GUID diferente para seu pacote. Os resultados de GUIDGEN contêm caracteres minúsculos, observe que você deve alterar todos os caracteres minúsculos para letras maiúsculas para um código de pacote válido. Consulte [códigos de pacote](package-codes.md).             |
| [**Contagem de páginas**](page-count-summary.md)(versão mínima do instalador)<br/> | 200                                    | Para um mínimo Windows Installer 2,0, essa propriedade deve ser definida como o inteiro 200.                                                                                                                                                                                                                                                                                                                 |
| [**Contagem de palavras**](word-count-summary.md)(tipo de origem)<br/>            | 0                                      | O tipo de origem global para o pacote são nomes de arquivo longos e não compactados. Consulte [fontes compactadas e descompactadas](compressed-and-uncompressed-sources.md) e a descrição da coluna atributos da [tabela de arquivos](file-table.md) para obter mais informações.                                                                                                                                |



 

As propriedades de fluxo de informações de resumo restantes não são necessárias, mas devem ser definidas para o exemplo de MNP2000.msi.



| Propriedade de informações de resumo                                 | Dados                                                                             | Observações                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Título**](title-summary.md)                               | Banco de dados de instalação                                                            | Informa aos usuários que esse banco de dados destina-se a uma instalação em vez de uma transformação ou um patch.                        |
| [**Assunto**](subject-summary.md)                           | MNP2000                                                                          | Os navegadores de arquivos podem exibir isso como o produto a ser instalado com esse banco de dados.                                  |
| [**Palavras-chave**](keywords-summary.md)                         | Instalador, MSI, banco de dados                                                         | Navegadores de arquivos com capacidade de pesquisa de palavra-chave podem pesquisar essas palavras.                                    |
| [**Autor**](author-summary.md)                             | Microsoft Corporation                                                            | Nome do fabricante do produto.                                                                                |
| [**Comentários**](comments-summary.md)                         | Este banco de dados do instalador contém a lógica e os requisitos necessários para instalar o bloco de notas. | Informa os usuários sobre a finalidade deste banco de dados.                                                                  |
| [**Criando aplicativo**](creating-application-summary.md) | Orca                                                                             | Aplicativo usado para criar o banco de dados de instalação. O exemplo especifica o editor de banco de dados Orca como um exemplo. |
| [**Segurança**](security-summary.md)                         | 0                                                                                | O banco de dados de exemplo é de leitura/gravação irrestrita.                                                                    |



 

Não é necessário definir as propriedades data/hora da última gravação [**salvas por**](last-saved-by-summary.md), [**última vez/dia**](last-saved-time-date-summary.md), [**criar data/hora**](create-time-date-summary.md), [**última impressão**](last-printed-summary.md), [**contagem de caracteres**](character-count-summary.md)e Resumo de [**página de código**](codepage-summary.md) para concluir este banco de dados de exemplo. O exemplo se baseia na ferramenta de edição de banco de dados para definir e atualizar essas propriedades opcionais.

Por exemplo, para usar MsiInfo para adicionar as informações de resumo ao exemplo, altere para o diretório que contém o banco de dados e use a linha de comando a seguir. Não reutilize a ID de pacote de exemplo mostrada abaixo.

**Msiinfo.exe MNP2000.msi-T "banco de dados de instalação"-J Subject-A "Microsoft Corporation"-K "instalador, MSI, banco de dados"-O "este banco de dados do instalador contém a lógica e os requisitos necessários para instalar o bloco de notas."-P; 1033-V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3}-G 200-W 0-N Orca-U 0**

Para obter mais detalhes sobre informações de resumo, consulte [sobre o fluxo de informações de resumo](about-the-summary-information-stream.md), [usando o fluxo de informações de resumo](using-the-summary-information-stream.md)e [referência de fluxo de informações de resumo](summary-information-stream-reference.md).

Consulte a [Propriedade fluxo de informações de resumo definida](summary-information-stream-property-set.md) para obter uma lista completa de todas as propriedades de informações de resumo e [descrições de propriedades de resumo](summary-property-descriptions.md) para sua descrição.

[Continuar](importing-the-user-interface.md)

 

 




