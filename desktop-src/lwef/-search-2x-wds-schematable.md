---
title: Esquema (recursos Windows ambiente herdado)
description: O esquema documenta os valores e as propriedades que o índice usa para armazenar dados para indexação ou classificação.
ms.assetid: dfd8862c-8f84-441e-a4b4-4af3c76c48f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d5c80690914073af1c67e2bd00376974547d30c4dc487c0656d4452d3fe828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753145"
---
# <a name="schema"></a>Esquema

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search.](../search/-search-3x-wds-overview.md)

O esquema documenta os valores e as propriedades que o índice usa para armazenar dados para indexação ou classificação. A tabela Esquema lista as colunas e suas propriedades (tipo e propid) incluídas no esquema do WDS (Pesquisa de Área de Trabalho do Microsoft Windows) 2.6.5.

## <a name="schema"></a>Esquema



| Nome da coluna                  | Descrição                                                                                                             | Propid                                                            |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| DocComments                  | Comentários                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/6                            |
| Criar                       | Data e hora em que o arquivo foi criado                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/15                           |
| DisplayFolder                | Pasta amigável para o item                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DisplayFolder                |
| DocAuthor                    | Autor do documento                                                                                                  | F29F85E0-4FF9-1068-AB91-08002B27B3D9/4                            |
| DocCategory                  | Categoria                                                                                                                | D5CDD502-2E9C-101B-9397-08002B2CF9AE/2                            |
| DocKeywords                  | Palavras-chave                                                                                                                | F29F85E0-4FF9-1068-AB91-08002B27B3D9/5                            |
| DocTitlePrefix               | Prefixo da assunto (Re:, Fw:, etc.)                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DocTitlePrefix               |
| DocTitle                     | Título                                                                                                                   | F29F85E0-4FF9-1068-AB91-08002B27B3D9/2                            |
| FileExtDesc                  | Descrição amigável do tipo de arquivo do Registro (por ex. .psq --> Arquivo de Consulta do Product Studio)                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExtDesc                  |
| FolderName                   | Nome da pasta pai                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FolderName                   |
| IsAttachment                 | Indica que o item é um anexo                                                                                         | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsAttachment                 |
| IsDeleted                    | Indica que o item está marcado para exclusão (lixeira, itens excluídos etc.)                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsDeleted                    |
| LastViewed                   | Data em que o item foi exibido pela última vez pelo usuário                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastViewed                   |
| Pessoas                       | Pessoas envolvidas com este item                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/People                       |
| PerceivedType                | PerceivedType do objeto OBSERVAÇÃO: isso é apenas para recuperação.                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType                |
| PerceivedTypeName            | Nome de exibição do PerceivedType.  Nunca exibido ou consultado                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedTypeName            |
| PrimaryDate                  | Data mais interessante (hora da última gravação para arquivos, data recebida para email)                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryDate                  |
| Tamanho                         | Tamanho de um arquivo.                                                                                                         | B725F130-47EF-101A-A5F1-02608C9EEBAC/12                           |
| DocSubject                   | Assunto do arquivo. OBSERVAÇÃO: atualmente, os assuntos de email são mapeados para PrimaryTitle hoje e não são duplicados devido ao tamanho | F29F85E0-4FF9-1068-AB91-08002B27B3D9/3                            |
| URL                          | URL baseada em consulta                                                                                                         | 49691C90-7E17-101A-A91C-08002B2ECDA9/9                            |
| Gravar                        | Data e hora da última gravação no arquivo                                                                             | B725F130-47EF-101A-A5F1-02608C9EEBAC/14                           |
| DueDate                      | Data em que um item é devido                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DueDate                      |
| IsIncomplete                 | Indica que o item não está totalmente disponível                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsIncomplete                 |
| IsFlaggedCompleted           | Indica que o item está sinalizado como concluído                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlaggedCompleted           |
| IsFlagged                    | Indica que o item está sinalizado                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsFlagged                    |
| FlagText                     | Texto exibido para o sinalizador, por exemplo, Revisão, Acompanhamento etc.                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FlagText                     |
| Identidade                     | Identidade para usuários do OE                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Identity                     |
| IsRead                       | Indica que o item foi lido                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRead                       |
| Importância                   | Importância ou prioridade do MAPI                                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Importance                   |
| ContainerHash                | Código hash que identifica os anexos a serem excluídos com base em uma URL de contêiner comum                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/ContainerHash                |
| DocFormat                    | Formato de documento ou MIMETYPE (por exemplo, ' message/rfc822 ' para um arquivo EML)                                              | 0B63E350-9CCC-11D0-BCDB-00805FCCCE04/5                            |
| GatherTimeModified           | Hora em que o indexador rastreou o documento pela última vez para a atualização do catálogo                                                           | 0b63e350-9ccc-11D0-bcdb-00805fccce04/4                            |
| Repositório                        | O manipulador de armazenamento ou de protocolo (arquivo, email, OUTLOOKEXPRESS)                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/armazenamento                        |
| FileExt                      | Extensão de arquivo                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FileExt                      |
| FileName                     | Nome do arquivo                                                                                                        | B725F130-47EF-101A-A5F1-02608C9EEBAC/10                           |
| ShortName                    | Nome de arquivo curto (8,3) para o arquivo                                                                                      | B725F130-47EF-101A-A5F1-02608C9EEBAC/20                           |
| Anexos              | Nomes de anexos em uma mensagem                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/anexos              |
| BccAddress                   | Endereços no campo Cco:                                                                                                 | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccAddress                   |
| BccName                      | Nomes de pessoas no campo Cco:                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BccName                      |
| CcAddress                    | Endereços no campo CC:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcAddress                    |
| CcName                       | Nomes de pessoas no campo CC:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CcName                       |
| Conversaid               | ID exclusiva de uma conversa em threads de email                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Conversaid               |
| FromAddress                  | Endereços no campo de:                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromAddress                  |
| FromName                     | Nome da pessoa no campo de:                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FromName                     |
| FwdRply                      | Indica que o email foi respondido ou encaminhado ( \_ ação cdoPR = 261 262)                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FwdRply                      |
| HasAttach                    | Indica que o email tem um anexo (T ou F)                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HasAttach                    |
| ReceivedDate                 | Tempo de entrega                                                                                                           | D5CDD505-2E9C-101B-9397-08002B2CF9AE/data de resficação                 |
| ToAddress                    | Endereços no campo para:                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/toAddress                    |
| NoName                       | Nomes de pessoas no campo para:                                                                                               | D5CDD505-2E9C-101B-9397-08002B2CF9AE/toName                       |
| TaskStatus                   | Status de uma tarefa                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TaskStatus                   |
| EndDate                      | Hora de término (geralmente para reuniões/eventos)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EndDate                      |
| IsRecurring                  | Indica que o item está recorrente (por exemplo, reuniões)                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IsRecurring                  |
| StartDate                    | Hora de início (geralmente para reuniões/eventos)                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/StartDate                    |
| Duration                     | Duração da reunião em minutos                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/duração                     |
| Location                     | Local em que ocorre o item (como uma reunião)                                                                             | D5CDD505-2E9C-101B-9397-08002B2CF9AE/local                     |
| Especiais                  | Data de aniversário                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/aniversário                  |
| AssistantName                | Nome do assistente                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantName                |
| AssistantTelephone           | Telefone do assistente                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/AssistantTelephone           |
| Birthday                     | Aniversário do contato                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/aniversário                     |
| BusinessAddressCity          | Informações de endereço comercial                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCity          |
| BusinessAddressPostalCode    | Informações de endereço comercial                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostalCode    |
| BusinessAddressPostOfficeBox | Informações de endereço comercial                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressPostOfficeBox |
| BusinessAddressState         | Informações de endereço comercial                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressState         |
| BusinessAddressDressDress        | Informações de endereço comercial                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressDress        |
| BusinessAddressCountry       | Informações de endereço comercial                                                                                                   | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessAddressCountry       |
| CallbackTelephone            | Informações de telefone de retorno de chamada                                                                                                | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CallbackTelephone            |
| CarTelephone                 | Informações de telefone                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CarTelephone                 |
| Children                     | Nomes de filhos para contato                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Children                     |
| CompanyMainTelephone         | Informações de telefone                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/CompanyMainTelephone         |
| EmailAddress                 | Nome do email de contato                                                                                                      | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailAddress                 |
| EmailName                    | Nome de exibição do endereço de email                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/EmailName                    |
| Nome                    | Nome do contato                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FirstName                    |
| FullName                     | Nome completo do contato                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/FullName                     |
| Sexo                       | Masculino/feminino/outro                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Gender                       |
| Hobby                        | Informações de contato                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/York                        |
| HomeAddressCity              | Informações de endereço residencial                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCity              |
| HomeAddressCountry           | Informações de endereço residencial                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressCountry           |
| HomeAddressPostalCode        | Informações de endereço residencial                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressPostalCode        |
| HomeAddressState             | Informações de endereço residencial                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressState             |
| HomeAddressStreet            | Informações de endereço residencial                                                                                                       | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeAddressDress            |
| HomeFaxNumber                | Informações de Facsimile                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeFaxNumber                |
| BusinessFaxNumber            | Informações de Facsimile                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/BusinessFaxNumber            |
| HomeTelephone                | Informações de telefone                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/HomeTelephone                |
| IMAddress                    | Informações instantâneas da mensagem                                                                                                    | D5CDD505-2E9C-101B-9397-08002B2CF9AE/IMAddress                    |
| JobTitle                     | Cargo do contato                                                                                                     | D5CDD505-2E9C-101B-9397-08002B2CF9AE/JobTitle                     |
| MiddleName                   | Informações de contato                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MiddleName                   |
| MobileTelephone              | Informações de telefone                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/MobileTelephone              |
| NickName                     | Informações de contato                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/NickName                     |
| Office                       | Informações de contato                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/Office                       |
| OfficeTelephone              | Informações de telefone                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/OfficeTelephone              |
| PagerTelephone               | Informações de telefone                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PagerTelephone               |
| LastName                     | Informações de contato                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/LastName                     |
| PersonalTitle                | Título da carreira (Dr., Mr., Mrs., Ms.)                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PersonalTitle                |
| PrimaryTelephone             | Informações de telefone                                                                                                          | D5CDD505-2E9C-101B-9397-08002B2CF9AE/PrimaryTelephone             |
| Profession                   | Informações de contato                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/                   |
| Cônjuge                       | Informações de contato                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/cônjuge                       |
| Sufixo                       | Informações de contato                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/sufixo                       |
| TelexNumber                  | Informações de telex                                                                                                              | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TelexNumber                  |
| TTYTDDTelephone              | Informações de TTY/TDD                                                                                                            | D5CDD505-2E9C-101B-9397-08002B2CF9AE/TTYTDDTelephone              |
| WebPage                      | Página de contato da Web                                                                                                        | D5CDD505-2E9C-101B-9397-08002B2CF9AE/página da Web                      |
| DocCompany                   | Empresa                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/15                           |
| DocLastAuthor                | Usuário o Doc wa salvo pela última vez por                                                                                           | F29F85E0-4FF9-1068-AB91-08002B27B3D9/8                            |
| DocLastPrinted               | Última Impressão                                                                                                            | F29F85E0-4FF9-1068-AB91-08002B27B3D9/11                           |
| DocManager                   | Gerente                                                                                                                 | D5CDD502-2E9C-101B-9397-08002B2CF9AE/14                           |
| DocPresentationFormat        | PresentationTarget                                                                                                      | D5CDD502-2E9C-101B-9397-08002B2CF9AE/3                            |
| DocSlideCount                | Slides                                                                                                                  | D5CDD502-2E9C-101B-9397-08002B2CF9AE/7                            |
| AudioAvgDataRate             | Taxa média de dados em Kbps para o arquivo de áudio                                                                            | 64440490-4C8B-11D1-8B70-080036B11A03/4                            |
| AudioTimeLength              | Comprimento em milissegundos do arquivo de áudio                                                                                | 56A3372E-CE9C-11D2-9F0E-006097C686F6/8                            |
| MusicAlbum                   | Nome do álbum                                                                                                              | 56A3372E-CE9C-11D2-9F0E-006097C686F6/4                            |
| MusicArtist                  | Nome do artista                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/2                            |
| MusicGenre                   | Gênero do álbum                                                                                                      | 56A3372E-CE9C-11D2-9F0E-006097C686F6/11                           |
| MusicTrack                   | Número de faixas no álbum                                                                                           | 56A3372E-CE9C-11D2-9F0E-006097C686F6/7                            |
| MusicYear                    | Ano em que o álbum foi registrado                                                                                    | 56A3372E-CE9C-11D2-9F0E-006097C686F6/5                            |
| ExifCameraMake               | Fabricante da câmera                                                                                                  | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/271                          |
| ExifCameraModel              | Modelo de câmera                                                                                                         | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/272                          |
| DateTaken                    | FILETIME de dados tirados                                                                                                  | D5CDD505-2E9C-101B-9397-08002B2CF9AE/DateTaken                    |
| ExifOrientation              | Orientation                                                                                                             | 14B81DA1-0135-4D31-96D9-6CBFC9671A99/274                          |
| ImageDimensions              | Dimensões da imagem                                                                                                 | 6444048F-4C8B-11D1-8B70-080036B11A03/13                           |
| ImageResX                    | Resolução X para a imagem                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/5                            |
| ImageResY                    | Resolução Y da imagem                                                                                              | 6444048F-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameHeight             | Altura do quadro do fluxo de vídeo                                                                                       | 64440491-4C8B-11D1-8B70-080036B11A03/4                            |
| VideoFrameRate               | Taxa de quadros em quadros por milissegundo para o fluxo de vídeo                                                               | 64440491-4C8B-11D1-8B70-080036B11A03/6                            |
| VideoFrameWidth              | Largura do quadro do fluxo de vídeo                                                                                        | 64440491-4C8B-11D1-8B70-080036B11A03/3                            |
| Classe                        | Nome da classe                                                                                                              | 8dee0300-16c2-101B-b121-08002b2ecda9/classe                        |
| Função                     | Nome da função                                                                                                           | 8dee0300-16c2-101B-b121-08002b2ecda9/Func                         |
| Estrutura                       | Nome da estrutura                                                                                                          | 8dee0300-16c2-101B-b121-08002b2ecda9/struct                       |
| Interface                    | Nome da interface                                                                                                          | 8dee0300-16c2-101B-b121-08002b2ecda9/interface                    |
| Delegar                     | Nome do representante                                                                                                           | 8dee0300-16c2-101B-b121-08002b2ecda9/delegado                     |
| Propriedade                     | Nome da propriedade                                                                                                           | 8dee0300-16c2-101B-b121-08002b2ecda9/Propriedade                     |
| Enumeração                         | Nome da enumeração                                                                                                               | 8dee0300-16c2-101B-b121-08002b2ecda9/enum                         |
| Const                        | Nome const                                                                                                              | 8dee0300-16c2-101B-b121-08002b2ecda9/const                        |
| Evento                        | Nome do evento                                                                                                              | 8dee0300-16c2-101B-b121-08002b2ecda9/evento                        |
| Campo                        | Nome do campo                                                                                                              | 8dee0300-16c2-101B-b121-08002b2ecda9/campo                        |
| Definir                       | Definir nome                                                                                                             | 8dee0300-16c2-101B-b121-08002b2ecda9/def                          |
| Componente                    | Nome do Componente                                                                                                          | 8dee0300-16c2-101B-b121-08002b2ecda9/componente                    |
| Projeto                      | Nome do projeto                                                                                                            | 8dee0300-16c2-101B-b121-08002b2ecda9/projeto                      |
| Solução                     | Nome da solução                                                                                                           | 8dee0300-16c2-101B-b121-08002b2ecda9/solução                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Desenvolvendo suplementos do IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desenvolvendo manipuladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

[Sintaxe de consulta avançada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[Tipos observados](-search-2x-wds-perceivedtype.md)
</dt> </dl>

 

 




