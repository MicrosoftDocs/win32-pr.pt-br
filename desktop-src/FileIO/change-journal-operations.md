---
description: Códigos de controle e estruturas para usar com o diário de alterações do USN (número de sequência de atualização) do sistema de arquivos NTFS.
ms.assetid: 2215f0d4-6ac8-42a5-87a5-9c76d1fae3ed
title: Operações de diário de alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a52cda51d0efc4cbae1333fc197f42d6a5cc0f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785467"
---
# <a name="change-journal-operations"></a><span data-ttu-id="777f3-103">Operações de diário de alterações</span><span class="sxs-lookup"><span data-stu-id="777f3-103">Change Journal Operations</span></span>

<span data-ttu-id="777f3-104">A lista a seguir identifica os códigos de controle que funcionam com o diário de alterações do USN (número de sequência de atualização) do sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="777f3-104">The following list identifies the control codes that work with the NTFS file system update sequence number (USN) change journal.</span></span>

-   [<span data-ttu-id="777f3-105">**FSCTL \_ criar \_ diário de USN \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-105">**FSCTL\_CREATE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal)
-   [<span data-ttu-id="777f3-106">**FSCTL \_ excluir \_ diário de USN \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-106">**FSCTL\_DELETE\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal)
-   [<span data-ttu-id="777f3-107">**\_ \_ dados USN de enumeração fsctl \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-107">**FSCTL\_ENUM\_USN\_DATA**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)
-   [<span data-ttu-id="777f3-108">**\_alça de marca de fsctl \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-108">**FSCTL\_MARK\_HANDLE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_mark_handle)
-   [<span data-ttu-id="777f3-109">**\_diário de \_ USN de consulta fsctl \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-109">**FSCTL\_QUERY\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal)
-   [<span data-ttu-id="777f3-110">**FSCTL \_ ler \_ \_ diário USN**</span><span class="sxs-lookup"><span data-stu-id="777f3-110">**FSCTL\_READ\_USN\_JOURNAL**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal)

<span data-ttu-id="777f3-111">A lista a seguir identifica as informações de estruturas relacionadas ao diário de alterações USN do sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="777f3-111">The following list identifies the structures information that relates to the NTFS file system USN change journal.</span></span>

-   [<span data-ttu-id="777f3-112">**CRIAR \_ \_ dados de diário de USN \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-112">**CREATE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data)
-   [<span data-ttu-id="777f3-113">**EXCLUIR \_ \_ dados de diário de USN \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-113">**DELETE\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-delete_usn_journal_data)
-   [<span data-ttu-id="777f3-114">**\_informações de alça de marca \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-114">**MARK\_HANDLE\_INFO**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mark_handle_info)
-   [<span data-ttu-id="777f3-115">**\_dados de enumeração de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-115">**MFT\_ENUM\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-mft_enum_data_v0)
-   [<span data-ttu-id="777f3-116">**LER \_ \_ dados do diário USN \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-116">**READ\_USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-read_usn_journal_data_v0)
-   [<span data-ttu-id="777f3-117">**\_dados do diário de USN \_**</span><span class="sxs-lookup"><span data-stu-id="777f3-117">**USN\_JOURNAL\_DATA**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0)
-   [<span data-ttu-id="777f3-118">**\_registro USN**</span><span class="sxs-lookup"><span data-stu-id="777f3-118">**USN\_RECORD**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2)

 

 
