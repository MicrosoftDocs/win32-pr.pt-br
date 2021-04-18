---
description: Este tópico descreve os itens que o Windows Search indexa.
ms.assetid: vs|search|~\search\wds3x\overviews\misc_items_in_index.htm
title: O que está incluído no índice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5560a14e3537c8e3ac8c7544aa7ffc9a0bc1bc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765665"
---
# <a name="what-is-included-in-the-index"></a>O que está incluído no índice

Este tópico descreve os itens que o Windows Search indexa.

Este tópico é organizado da seguinte maneira:

-   [Indexado por padrão](#indexed-by-default)
-   [Formatos de arquivo com suporte](#file-formats-supported)
-   [Exclusões de arquivo](#file-exclusions)
-   [Exclusões de pastas](#folder-exclusions)
-   [Exclusões de unidade](#drive-exclusions)
-   [Tópicos relacionados](#related-topics)

 

## <a name="indexed-by-default"></a>Indexado por padrão

Os manipuladores de protocolo e os filtros estão incluídos no Windows Search para indexar os seguintes tipos de conteúdo:

-   No Windows Vista e posterior, os itens de email do Microsoft Outlook e do Microsoft Outlook Express de um usuário são indexados enquanto o aplicativo de email está em execução.
-   Os arquivos offline no cache do lado do cliente (CSC) são indexados pelo Windows Search localmente.
-   O Windows Search dá suporte à coleta de endereços de início do arquivo em volumes NTFS e FAT32. O NTFS dá suporte à indexação baseada em notificação e o FAT32 dá suporte a um rastreamento incremental na inicialização e, em seguida, responde às notificações.
-   O Windows Vista e posteriores continuam a expor uma propriedade por pasta/por arquivo para habilitar a indexação: a opção "**para pesquisa rápida, permitindo que o serviço de indexação indexe esta pasta**" na caixa de diálogo de **Propriedades** . Definir o sinalizador de bits de forma estranha garante que as propriedades básicas do protocolo, como URL, nome de arquivo e tamanho, sejam indexadas, mas que nenhum manipulador de filtro nem manipuladores de propriedade sejam executados.
-   O conteúdo do texto é indexado, mas a pontuação não é.

## <a name="file-formats-supported"></a>Formatos de arquivo com suporte

O Windows Search tem manipuladores de protocolo, manipuladores de propriedade e manipuladores de filtro para indexar os seguintes formatos automaticamente:

-   Arquivos de mídia: todos os tipos de arquivo de mídia
-   **HTML** (nlhtml.dll):. ascx,. asp,. aspx,. CSS,. HHC,. htm,. html,. htt,. htw,. htx,. odc,. stm
-   **HTML MIME** (mimefilt.dll):. mht,. mhtml
-   **Office** (offfilt.dll):. doc,. dot,. pot,. PPS,. ppt,. xlb,. xlc,. xls,. xlt
-   **Text** (query.dll):. asm,. ASX,. bat,. c,. cmd,. cpp,. cxx,. def,. dic,. h,. HPP,. hXX,. idl,. idq,. inf,. ini,. inx,. js,. log,. m3u,. rc,. reg,. rtf,. txt,. URL,. vbs,. WTX
-   **XML** (xmlfilt.dll):. xml,. xsl
-   **OneNote**:. One
-   **Diário do Tablet** (jntfiltr.dll):. jnt

As propriedades são indexadas para todos os arquivos, exceto o armazenamento estruturado. No Windows Vista e posterior, muitas propriedades de arquivo de mídia são indexadas; no entanto, o conteúdo não será indexado se os arquivos forem protegidos pelo DRM (gerenciamento de direitos digitais).

> [!Note]  
> O filtro HTML não indexa comentários HTML.

 

## <a name="file-exclusions"></a>Exclusões de arquivo

Quando um tipo de arquivo não tem um filtro associado, ou quando um arquivo não tem uma extensão, as propriedades do sistema para arquivos desse tipo são indexadas, mas o conteúdo do arquivo não é indexado.

Além disso, o Windows Search não indexa o conteúdo de arquivos em gerenciamento de direitos de informação (IRM) ou DRM (gerenciamento de direitos digitais).

No Windows Vista (somente), os seguintes arquivos são excluídos da indexação por padrão:

-   Arquivos marcados como ocultos ou do sistema.
-   Arquivos com as seguintes extensões:

    .386,. APS,. AudioCD,. bin,. Bk1,. bk2,. bkf,. BSC,. BTR,. chk,. CI,. crwl,. dbg,. DCT,. DeskLink,. dir,. dl \_ ,. dll,. drv,. DVD,. evt,. ex \_ ,. exe,. exp,. EYB,. fnd,. fnt,. Folder,. Fon,. GHI,. gthr,. hqx,. ICM,. idb,. idx,. ilk,. IMC,. em \_ ,. ini,. inv,. JBF,. LaTeX,. lib,. local,. M14,. Mac,. manifest,. map,. MAPIMail,. MMF,. Movie,. MV,. mydocs,. NCB,. obj,. oC \_ ,. ocx,. pch,. pdb,. PF,. PMA,. PMC,. PML,. PMR,. res,. RMP,. RPC,. rsp,. SBR,. SC2,. sit,. Sr \_ ,. Sy \_ ,. sym,. sys,. tlb,. trc,. TTC,. ttf,. VBX,. vxd,. wll,. WLT,. XIX,. Z96,. ZFSendToTarget.

## <a name="folder-exclusions"></a>Exclusões de pastas

> [!TIP]
> Os nomes de pastas não diferenciam maiúsculas de minúsculas.

 

As seguintes pastas são excluídas da indexação por padrão:



| Padrão de exclusão de pasta                                                              | Efeito no Windows 7 | Efeito no Windows Vista | Description                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------|---------------------|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *% System%* \\ ProgramData \\ \\ dados de pesquisa da Microsoft \\\\                                    | **Excluído**        | Sem efeito               | Dados do indexador na unidade do sistema.                                                                                                                                                                                          |
| *% System%* \\ Usuários \\ *nome de usuário* \\ AppData\\                                              | **Excluído**        | Sem efeito               | Dados de aplicativo do usuário (inclui dados temporários) na unidade do sistema.<br/> Para cada usuário que faz logon no sistema, é adicionado um padrão de exclusão específico que exclui os dados do aplicativo do índice.<br/> |
| *% System%* \\ Usuários de \\ \* \\ AppData \\ locais \\ arquivos da \\ \\ Internet temporários do Microsoft Windows\\ | **Excluído**        | Sem efeito               | Local padrão dos arquivos temporários da Internet do Windows Internet Explorer na unidade do sistema.<br/> Se o local dos arquivos temporários da Internet do Internet Explorer for alterado, esses arquivos poderão ser indexados.<br/>    |
| *% System%* \\ CSC do Windows \\\\                                                            | **Excluído**        | Sem efeito               | Se a indexação estiver ativada para o diretório do sistema do Windows, a pasta CSC (na unidade do sistema) ainda será excluída da indexação.                                                                                           |
| *% System%* \\ Temp do Windows \\ \* \\\\                                                       | **Excluído**        | Sem efeito               | Dados temporários do Windows na unidade do sistema.                                                                                                                                                                                     |
| *% System%* \\ Windows.\*\\                                                              | **Excluído**        | Sem efeito               | Instalações antigas do Windows na unidade do sistema.                                                                                                                                                                             |
| *% System%* \\ ProgramData\\                                                             | **Excluído**        | **Excluído**            | Observe que a subpasta do menu iniciar compartilhado é indexada.                                                                                                                                                                     |
| *% System%* \\ Usuários \\ \* \\ AppData\\                                                      | **Excluído**        | **Excluído**            | Dados de aplicativo dos usuários (inclui dados temporários).                                                                                                                                                                              |
| *% System%* \\ Usuários de \\ \* \\ AppData \\ local \\ temporário\\                                         | **Excluído**        | **Excluído**            | Dados temporários dos usuários. Se a indexação estiver ativada para dados de aplicativo do usuário, os dados temporários do usuário ainda serão excluídos da indexação por padrão.                                                                                           |
| *% System%* \\ Windows\\                                                                 | **Excluído**        | **Excluído**            | Arquivos do sistema operacional na unidade do sistema.                                                                                                                                                                                |
| *% System%* \\ $Recycle Bin\\                                                            | **Excluído**        | **Excluído**            | Local dos arquivos na lixeira.                                                                                                                                                                                      |
| *% System%* \\ Integrado\\                                                                   | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *% System%* \\ Repositório instalado\\                                                    | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *% System%* \\ Arquivos de programas\\                                                           | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| *% System%* \\ Arquivos de programas (x86)\\                                                     | Sem efeito           | **Excluído**            | Na unidade do sistema.                                                                                                                                                                                                       |
| \*\\Temp\\\*                                                                          | Sem efeito           | **Excluído**            | Dados temporários do Windows e outras pastas com o nome "Temp".                                                                                                                                                                  |
| *% System%* \\ Usuários \\ padrão\\                                                          | Sem efeito           | **Excluído**            | O local dos dados de perfil de usuário padrão na unidade do sistema.                                                                                                                                                             |
| \*\\Windows.\*\\                                                                      | Sem efeito           | **Excluído**            | Instalações antigas do Windows e outras pastas com nomes que começam com "Windows".                                                                                                                                         |



 

## <a name="drive-exclusions"></a>Exclusões de unidade

No Windows 7 e no Windows Vista, as unidades removíveis não são indexadas por padrão.

> [!Note]  
> Se as unidades removíveis se reportarem como unidades fixas, você poderá adicioná-las a serem indexadas mesmo que elas sejam realmente removíveis. As informações permanecerão no índice e o Windows Search fará um rastreamento incremental para reconciliar os resultados de indexação quando o disco removível for conectado novamente. Como as unidades flash USB se reportam como removíveis, elas não podem ser indexadas.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Indexação, consulta e notificações no Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Processo de indexação no Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Processo de consulta no Windows Search](querying-process--windows-search-.md)
</dt> <dt>

[Processo de notificações no Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisitos de formatação de URL](url-formatting-requirements.md)
</dt> </dl>

 

 




