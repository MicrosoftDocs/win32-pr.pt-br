---
title: Funções de retorno de chamada ProjFS
description: As seguintes funções de retorno de chamada são declaradas em projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/22/2020
ms.locfileid: "103823531"
---
# <a name="callback-functions"></a><span data-ttu-id="553d5-103">Funções de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="553d5-103">Callback functions</span></span>

<span data-ttu-id="553d5-104">As seguintes funções de retorno de chamada são declaradas em projectedfslib. h.</span><span class="sxs-lookup"><span data-stu-id="553d5-104">The following callback functions are declared in projectedfslib.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="553d5-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="553d5-105">In this section</span></span>

| <span data-ttu-id="553d5-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="553d5-106">Topic</span></span> | <span data-ttu-id="553d5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="553d5-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="553d5-108">**PRJ_CANCEL_COMMAND_CB**</span><span class="sxs-lookup"><span data-stu-id="553d5-108">**PRJ_CANCEL_COMMAND_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | <span data-ttu-id="553d5-109">Notifica o provedor de que uma operação por uma invocação anterior de um retorno de chamada deve ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="553d5-109">Notifies the provider that an operation by an earlier invocation of a callback should be canceled.</span></span> |
| [<span data-ttu-id="553d5-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="553d5-110">**PRJ_END_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | <span data-ttu-id="553d5-111">Informa ao provedor que uma enumeração de diretório está acima.</span><span class="sxs-lookup"><span data-stu-id="553d5-111">Informs the provider that a directory enumeration is over.</span></span> |
| [<span data-ttu-id="553d5-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="553d5-112">**PRJ_GET_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | <span data-ttu-id="553d5-113">Solicita informações de enumeração de diretório do provedor.</span><span class="sxs-lookup"><span data-stu-id="553d5-113">Requests directory enumeration information from the provider.</span></span>
| [<span data-ttu-id="553d5-114">**PRJ_GET_FILE_DATA_CB**</span><span class="sxs-lookup"><span data-stu-id="553d5-114">**PRJ_GET_FILE_DATA_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | <span data-ttu-id="553d5-115">Solicita o conteúdo do fluxo de dados primário de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="553d5-115">Requests the contents of a file's primary data stream.</span></span>
| [<span data-ttu-id="553d5-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span><span class="sxs-lookup"><span data-stu-id="553d5-116">**PRJ_GET_PLACEHOLDER_INFO_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | <span data-ttu-id="553d5-117">Solicita informações para um arquivo ou diretório do provedor.</span><span class="sxs-lookup"><span data-stu-id="553d5-117">Requests information for a file or directory from the provider.</span></span>
| [<span data-ttu-id="553d5-118">**PRJ_NOTIFICATION_CB**</span><span class="sxs-lookup"><span data-stu-id="553d5-118">**PRJ_NOTIFICATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | <span data-ttu-id="553d5-119">Fornece notificações para o provedor sobre operações do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="553d5-119">Delivers notifications to the provider about file system operations.</span></span>
| [<span data-ttu-id="553d5-120">**PRJ_QUERY_FILE_NAME_CB**</span><span class="sxs-lookup"><span data-stu-id="553d5-120">**PRJ_QUERY_FILE_NAME_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | <span data-ttu-id="553d5-121">Determina se um determinado caminho de arquivo existe no repositório de backup do provedor.</span><span class="sxs-lookup"><span data-stu-id="553d5-121">Determines whether a given file path exists in the provider's backing store.</span></span>
| [<span data-ttu-id="553d5-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span><span class="sxs-lookup"><span data-stu-id="553d5-122">**PRJ_START_DIRECTORY_ENUMERATION_CB**</span></span>](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | <span data-ttu-id="553d5-123">Informa ao provedor que uma enumeração de diretório está iniciando.</span><span class="sxs-lookup"><span data-stu-id="553d5-123">Informs the provider that a directory enumeration is starting.</span></span>