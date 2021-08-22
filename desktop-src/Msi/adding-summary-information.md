---
description: As propriedades de informações resumidas a seguir devem ser definidas em cada pacote de instalação, usando uma ferramenta de software para acessar a interface Istream do Fluxo de Informações de Resumo.
ms.assetid: 9775959f-5ab2-43cd-8cc8-9d81945b4ec6
title: Adicionando informações resumidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dc43ba8df737fb4d7c30998ec6c9581376df6ef6274140e68ec767e3a416f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328576"
---
# <a name="adding-summary-information"></a>Adicionando informações resumidas

As propriedades de informações resumidas a seguir devem ser definidas em cada pacote de instalação, usando uma ferramenta de software para acessar a interface **Istream** do [Fluxo de Informações de Resumo](summary-information-stream.md). Por exemplo, você pode usar a ferramenta Msiinfo.exe fornecida com o SDK do Windows Installer para definir essas propriedades. Se essas propriedades não estão definidas, o pacote não passará na [Validação de Pacote.](package-validation.md)



| Propriedade de informações de resumo                                                   | Dados                                   | Observações                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modelo**](template-summary.md)(plataforma e linguagem)<br/>         | ;1033                                  | Plataforma e idioma usados pelo banco de dados. Se a especificação da plataforma estiver ausente no valor da propriedade [**Resumo**](template-summary.md) do Modelo, o instalador assumirá a arquitetura da Intel. A [**propriedade ProductLanguage**](productlanguage.md) do banco de dados normalmente é usada para essa propriedade de resumo. A ID de idioma do exemplo indica que o pacote usa o inglês dos EUA. |
| [**Número de revisão**](revision-number-summary.md)(código do pacote)<br/>    | {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} | Esse é o GUID do código [do](guid.md) pacote que identifica exclusivamente o pacote de exemplo. Se você reproduzir este exemplo, use um utilitário como GUIDGEN para gerar um GUID diferente para seu pacote. Os resultados de GUIDGEN contêm caracteres minúsculos, observe que você deve alterar todos os caracteres minúsculos para maiúsculas para um código de pacote válido. Consulte [Códigos de pacote](package-codes.md).             |
| [**Contagem de páginas**](page-count-summary.md)(versão mínima do instalador)<br/> | 200                                    | Para um mínimo Windows 2.0, essa propriedade deve ser definida como o inteiro 200.                                                                                                                                                                                                                                                                                                                 |
| [**Contagem de palavras**](word-count-summary.md)(tipo de origem)<br/>            | 0                                      | O tipo de origem global para o pacote são nomes de arquivo longos e descompactados. Consulte [Fontes compactadas e descompactados](compressed-and-uncompressed-sources.md) e a descrição da coluna Atributos da tabela [Arquivo](file-table.md) para obter mais informações.                                                                                                                                |



 

As propriedades restantes do fluxo de informações resumidas não são necessárias, mas devem ser definidas para o MNP2000.msi exemplo.



| Propriedade de informações de resumo                                 | Dados                                                                             | Observações                                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**Título**](title-summary.md)                               | Banco de dados de instalação                                                            | Informa aos usuários que esse banco de dados é para uma instalação em vez de uma transformação ou um patch.                        |
| [**Assunto**](subject-summary.md)                           | MNP2000                                                                          | Os navegadores de arquivos podem exibir isso como o produto a ser instalado com esse banco de dados.                                  |
| [**Palavras-chave**](keywords-summary.md)                         | Instalador, MSI, Banco de Dados                                                         | Navegadores de arquivos que são capazes de pesquisar palavras-chave podem pesquisar essas palavras.                                    |
| [**Autor**](author-summary.md)                             | Microsoft Corporation                                                            | Nome do fabricante do produto.                                                                                |
| [**Comentários**](comments-summary.md)                         | Esse banco de dados do instalador contém a lógica e os dados necessários para instalar Bloco de notas. | Informa os usuários sobre a finalidade desse banco de dados.                                                                  |
| [**Criando aplicativo**](creating-application-summary.md) | Orca                                                                             | Aplicativo usado para criar o banco de dados de instalação. O exemplo especifica o editor de banco de dados Orca como um exemplo. |
| [**Segurança**](security-summary.md)                         | 0                                                                                | O banco de dados de exemplo é leitura/gravação irrestrita.                                                                    |



 

Você não precisa definir as propriedades de resumo Última Salva por [**,**](last-saved-by-summary.md)Hora/Data da Última Salvação, [**Hora/Data**](last-saved-time-date-summary.md) [**de**](create-time-date-summary.md)Criação [**,**](last-printed-summary.md)Última [**Impressa,**](character-count-summary.md)Contagem de Caracteres e [**Página**](codepage-summary.md) de Código para concluir este banco de dados de exemplo. O exemplo depende da ferramenta de edição de banco de dados para definir e atualizar essas propriedades opcionais.

Por exemplo, para usar msiInfo para adicionar as informações resumidas ao exemplo, altere para o diretório que contém o banco de dados e use a linha de comando a seguir. Não reutilizar a ID do pacote de exemplo mostrada abaixo.

**Msiinfo.exe MNP2000.msi -T "Banco de Dados de Instalação" -J Assunto -A "Microsoft Corporation" -K "Instalador, MSI, Database" -O "Este banco de dados do instalador contém a lógica e os dados necessários para instalar o Bloco de notas." -P ;1033 -V {4966AEC4-3C59-4B07-9B98-1B6A7103C0D3} -G 200 -W 0 -N Orca -U 0**

Para obter mais detalhes sobre informações resumidas, consulte Sobre o [fluxo de](about-the-summary-information-stream.md)informações de resumo , Usando o [fluxo](using-the-summary-information-stream.md)de informações de resumo e Referência do fluxo de informações de [resumo](summary-information-stream-reference.md).

Consulte o [Conjunto de Propriedades do Fluxo de](summary-information-stream-property-set.md) Informações de Resumo para obter uma lista completa de todas as propriedades de informações resumidas e Descrições da propriedade [Summary](summary-property-descriptions.md) para obter sua descrição.

[Continuar](importing-the-user-interface.md)

 

 




