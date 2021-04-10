---
description: Descreve como os pontos de nova análise permitem o comportamento do sistema de arquivos que faz parte do comportamento que a maioria dos desenvolvedores do Windows espera.
ms.assetid: 1aaebda9-0013-4282-9ae1-7c829e171942
title: Pontos de nova análise e operações de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1132197cd689157cd9f219afa5bfc1474b587c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170962"
---
# <a name="reparse-points-and-file-operations"></a><span data-ttu-id="ce333-103">Pontos de nova análise e operações de arquivo</span><span class="sxs-lookup"><span data-stu-id="ce333-103">Reparse Points and File Operations</span></span>

<span data-ttu-id="ce333-104">Os *pontos de nova análise* habilitam o comportamento do sistema de arquivos que faz parte do comportamento em que a maioria dos desenvolvedores do Windows pode estar acostumado, portanto, estar ciente desses comportamentos ao escrever aplicativos que manipulam arquivos é vital para aplicativos robustos e confiáveis destinados a acessar sistemas de arquivos que dão suporte a pontos de nova análise.</span><span class="sxs-lookup"><span data-stu-id="ce333-104">*Reparse points* enable file system behavior that departs from the behavior most Windows developers may be accustomed to, therefore being aware of these behaviors when writing applications that manipulate files is vital to robust and reliable applications intended to access file systems that support reparse points.</span></span> <span data-ttu-id="ce333-105">A extensão dessas considerações dependerá da implementação específica e do comportamento do filtro do sistema de arquivos associado de um determinado ponto de nova análise, que pode ser definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ce333-105">The extent of these considerations will depend on the specific implementation and associated file system filter behavior of a particular reparse point, which can be user-defined.</span></span> <span data-ttu-id="ce333-106">Para obter mais informações, consulte [pontos de nova análise](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="ce333-106">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="ce333-107">Considere os exemplos a seguir sobre as implementações de ponto de nova análise de NTFS, que incluem pastas montadas, arquivos vinculados e o servidor de armazenamento remoto da Microsoft:</span><span class="sxs-lookup"><span data-stu-id="ce333-107">Consider the following examples regarding NTFS reparse point implementations, which include mounted folders, linked files, and the Microsoft Remote Storage Server:</span></span>

-   <span data-ttu-id="ce333-108">Os aplicativos de backup que usam [fluxos de arquivos](file-streams.md) devem especificar **\_ \_ dados de nova análise de backup** na estrutura de [**\_ \_ ID de fluxo do Win32**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) ao fazer backup de arquivos com pontos de nova análise.</span><span class="sxs-lookup"><span data-stu-id="ce333-108">Backup applications that use [file streams](file-streams.md) should specify **BACKUP\_REPARSE\_DATA** in the [**WIN32\_STREAM\_ID**](/windows/desktop/api/winbase/ns-winbase-win32_stream_id) structure when backing up files with reparse points.</span></span>
-   <span data-ttu-id="ce333-109">Os aplicativos que usam a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) devem especificar o sinalizador do **sinalizador de arquivo \_ \_ abrir \_ \_ ponto de nova análise** ao abrir o arquivo se ele for um ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="ce333-109">Applications that use the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function should specify the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag when opening the file if it is a reparse point.</span></span> <span data-ttu-id="ce333-110">Para obter mais informações, consulte [criando e abrindo arquivos](creating-and-opening-files.md).</span><span class="sxs-lookup"><span data-stu-id="ce333-110">For more information, see [Creating and Opening Files](creating-and-opening-files.md).</span></span>
-   <span data-ttu-id="ce333-111">O processo de [desfragmentação de arquivos](defragmenting-files.md) requer tratamento especial para pontos de nova análise.</span><span class="sxs-lookup"><span data-stu-id="ce333-111">The process of [defragmenting files](defragmenting-files.md) requires special handling for reparse points.</span></span>
-   <span data-ttu-id="ce333-112">Os aplicativos de detecção de vírus devem procurar pontos de nova análise que indiquem arquivos vinculados.</span><span class="sxs-lookup"><span data-stu-id="ce333-112">Virus detection applications should search for reparse points that indicate linked files.</span></span>
-   <span data-ttu-id="ce333-113">A maioria dos aplicativos deve executar ações especiais para arquivos que foram movidos para o armazenamento de longo prazo, se apenas notificar o usuário de que pode levar algum tempo para recuperar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ce333-113">Most applications should take special actions for files that have been moved to long-term storage, if only to notify the user that it may take a while to retrieve the file.</span></span>
-   <span data-ttu-id="ce333-114">A função [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) abrirá o arquivo ou o ponto de nova análise, dependendo do uso do sinalizador de **\_ \_ \_ \_ ponto de nova análise aberto do sinalizador de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="ce333-114">The [**OpenFileById**](/windows/desktop/api/WinBase/nf-winbase-openfilebyid) function will either open the file or the reparse point, depending on the use of the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span>
-   <span data-ttu-id="ce333-115">Links simbólicos, como pontos de nova análise, têm determinadas [considerações de programação](symbolic-link-programming-considerations.md) específicas para eles.</span><span class="sxs-lookup"><span data-stu-id="ce333-115">Symbolic links, as reparse points, have certain [programming considerations](symbolic-link-programming-considerations.md) specific to them.</span></span>
-   <span data-ttu-id="ce333-116">As atividades de gerenciamento de volume para ler os registros do diário de alterações do USN (número de sequência de atualização) exigem tratamento especial para pontos de nova análise ao usar o [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) e ler estruturas de [**\_ dados do \_ diário \_ de USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) .</span><span class="sxs-lookup"><span data-stu-id="ce333-116">Volume management activities for reading update sequence number (USN) change journal records require special handling for reparse points when using the [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**READ\_USN\_JOURNAL\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce333-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce333-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce333-118">Determinando se um diretório é uma pasta montada</span><span class="sxs-lookup"><span data-stu-id="ce333-118">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)
</dt> <dt>

[<span data-ttu-id="ce333-119">Criando pastas montadas</span><span class="sxs-lookup"><span data-stu-id="ce333-119">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)
</dt> <dt>

[<span data-ttu-id="ce333-120">Efeitos de link simbólico em funções de sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="ce333-120">Symbolic Link Effects on File Systems Functions</span></span>](symbolic-link-effects-on-file-systems-functions.md)
</dt> </dl>

 

 
