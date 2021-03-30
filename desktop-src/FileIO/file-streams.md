---
description: No sistema de arquivos NTFS, os fluxos contêm os dados gravados em um arquivo, e isso fornece mais informações sobre um arquivo do que atributos e propriedades.
ms.assetid: 41dda6f1-a6d1-4e76-94f3-a72f9e491bee
title: Fluxos de arquivos (sistemas de arquivos locais)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a934a51225a886e3d5a7de4d9e1e91900fab460
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661797"
---
# <a name="file-streams-local-file-systems"></a>Fluxos de arquivos (sistemas de arquivos locais)

Um fluxo é uma sequência de bytes. No sistema de arquivos NTFS, os fluxos contêm os dados gravados em um arquivo, e isso fornece mais informações sobre um arquivo do que atributos e propriedades. Por exemplo, você pode criar um fluxo que contém palavras-chave de pesquisa ou a identidade da conta de usuário que cria um arquivo.

Cada fluxo associado a um arquivo tem seu próprio tamanho de alocação, tamanho real e comprimento de dados válido:

-   O tamanho da alocação é a quantidade de espaço em disco reservada para um fluxo.
-   O tamanho real é o número de bytes que estão sendo usados por um chamador.
-   O comprimento de dados válido (VDL) é o número de bytes inicializados a partir do tamanho de alocação para o fluxo.

Cada fluxo também mantém seu próprio estado para compactação, criptografia e sobregrosseira. O atributo de arquivo **\_ \_ \_ esparso de atributo** de arquivo no arquivo é definido no membro **dwFileAttributes** da estrutura de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) retornada das funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) se qualquer um dos fluxos já tiver sido esparso. [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa), [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa), [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda), [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)e [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) retornam o estado esparso do fluxo de dados padrão se nenhum fluxo for especificado.

Não há tempos de arquivo associados a um fluxo. Os horários de arquivo de um arquivo são atualizados quando qualquer fluxo em um arquivo é atualizado.

Os bloqueios oportunistas são mantidos por fluxo. Os modos de compartilhamento também são mantidos por fluxo. Quando o acesso de exclusão é solicitado em um arquivo, o sistema operacional verifica o acesso de exclusão em todos os fluxos abertos em um arquivo. Se outro processo tiver aberto um fluxo sem a permissão de **\_ \_ exclusão de compartilhamento de arquivo** , você não poderá abrir o arquivo para acesso de exclusão.

Se um arquivo que está sendo copiado tiver um fluxo de dados e o redirecionador de rede for usado, o arquivo só poderá ser copiado se o cliente tiver a permissão de leitura e a permissão ler atributos.

## <a name="naming-conventions-for-streams"></a>Convenções de nomenclatura para fluxos

Quando especificado na linha de comando do shell do Windows, o nome completo de um fluxo é "*filename*:*Stream Name*:*Stream Type*", como no exemplo a seguir: "myfile. dat: STREAM1: $data".

Todos os caracteres que são válidos para um nome de arquivo também são válidos para o nome do fluxo, incluindo espaços. Para obter mais informações, consulte [nomeando um arquivo](naming-a-file.md). O tipo de fluxo (também chamado de código de tipo de atributo) é interno ao sistema de arquivos NTFS. Portanto, os usuários não podem criar novos tipos de fluxo, mas podem abrir tipos de sistema de arquivos NTFS existentes. Os valores do especificador de tipo de fluxo sempre começam com o símbolo de cifrão ($). Veja abaixo uma lista de tipos de fluxo.

Por padrão, o fluxo de dados padrão não tem nome. Para especificar completamente o fluxo de dados padrão, use "*filename*:: $data", em que $data é o tipo de fluxo. Esse é o equivalente de "*filename*". Você pode criar um fluxo nomeado no arquivo usando as [convenções de nomenclatura de arquivo](naming-a-file.md). Observe que "$DATA" é um nome de fluxo legal. Por exemplo, o nome completo de um fluxo chamado "$DATA" em um arquivo chamado "*Sample*" seria "*Sample*: $Data: $data". Se você criou um fluxo chamado "barra" no mesmo arquivo, seu nome completo seria "*exemplo*: barra: $data".

Ao criar e trabalhar com arquivos com nomes de um caractere, Prefixe o nome do arquivo com o período seguido por uma barra invertida (. \) ou use um nome de caminho totalmente qualificado. O motivo para fazer isso é que o Windows trata nomes de arquivo de um caractere como letras de unidade. Quando uma letra de unidade é especificada com um caminho relativo, um caractere de dois pontos separa a letra da unidade do caminho. Quando há uma ambiguidade sobre se um nome de um caractere é uma letra de unidade ou um nome de arquivo, o Windows pressupõe que é uma letra de unidade se a cadeia de caracteres após os dois-pontos é um caminho válido, mesmo que a letra da unidade seja inválida.

## <a name="stream-types"></a>Tipos de fluxo

A seguir está a lista de tipos de fluxo NTFS, também chamados de códigos de tipo de atributo. Alguns dos tipos de fluxo são internos ao NTFS e seu formato não é documentado.



| Tipo de fluxo                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| :: lista de $ATTRIBUTE \_         | Contém uma lista de todos os atributos que compõem o arquivo e identifica onde cada atributo está localizado.                                                                                                                                                                                                                                                                                                                                          |
| :: $BITMAP                  | Um bitmap usado por índices para gerenciar o espaço livre da árvore b para um diretório. A árvore b é gerenciada em partes de 4 KB (independentemente do tamanho do cluster) e é usada para gerenciar a alocação dessas partes. Esse tipo de fluxo está presente em cada diretório.                                                                                                                                                                                           |
| :: $DATA                    | Fluxo de dados. O fluxo de dados padrão não tem nome. Os fluxos de dados podem ser enumerados usando as funções [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) e [**FindNextStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw) .                                                                                                                                                                                                                                                |
| :: $EA                      | Contém dados de atributos estendidos.|
| :: informações de $EA \_         | Contém informações de suporte sobre os atributos estendidos.                                                                                                                                                                                                                                                                                                                                                                                      |
| :: nome do $FILE \_              | O nome do arquivo, em caracteres Unicode. Isso inclui o nome curto do arquivo, bem como links físicos.                                                                                                                                                                                                                                                                                                                                 |
| :: $INDEX \_ alocação       | O tipo de fluxo de um diretório. Usado para implementar a alocação de nome de arquivo para diretórios grandes. Esse fluxo representa o próprio diretório e contém todos os dados do diretório. As alterações nos fluxos desse tipo são registradas no diário de alterações do NTFS. O nome de fluxo padrão de um \_ tipo de fluxo de alocação $index é de $I 30 para "*dirname*", "*dirname*:: $index \_ alocação" e "*dirname*: $I 30: $index \_ alocação" são equivalentes. |
| :: $INDEX \_ raiz             | Esse fluxo representa a raiz da árvore b de um índice. Esse tipo de fluxo está presente em cada diretório.                                                                                                                                                                                                                                                                                                                                           |
| :: $LOGGED \_ o \_ fluxo do utilitário | Semelhante a:: $DATA mas as operações são registradas no diário de alterações do NTFS. Usado pelo EFS e pelo [NTFS Transacional (TxF)](transactional-ntfs-portal.md). O par ":*StreamName*: $*streamtype*" para EFS é ": $EFS: \_ Stream do utilitário $logged \_ " e para TxF é ": $TxF \_ Data: $logged do \_ utilitário \_ Stream".                                                                                                                                                    |
| :: ID de $OBJECT \_              | Uma ID de 16 bytes usada para identificar o arquivo para o serviço de rastreamento de link.                                                                                                                                                                                                                                                                                                                                                                           |
| :: ponto de $REPARSE \_          | Os dados do [ponto de nova análise](reparse-points.md) .|



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando fluxos](using-streams.md)
</dt> </dl>

 

 



