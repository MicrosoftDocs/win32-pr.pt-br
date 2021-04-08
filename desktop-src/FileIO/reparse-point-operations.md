---
description: Descreve as operações de ponto de nova análise que você pode executar usando DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Operações de ponto de nova análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011530"
---
# <a name="reparse-point-operations"></a><span data-ttu-id="df177-103">Operações de ponto de nova análise</span><span class="sxs-lookup"><span data-stu-id="df177-103">Reparse Point Operations</span></span>

<span data-ttu-id="df177-104">Para determinar se um sistema de arquivos dá suporte a pontos de nova análise, chame a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examine se o **arquivo dá suporte ao sinalizador de bit de \_ \_ \_ pontos de nova análise** .</span><span class="sxs-lookup"><span data-stu-id="df177-104">To determine whether a file system supports reparse points, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FILE\_SUPPORTS\_REPARSE\_POINTS** bit flag.</span></span>

<span data-ttu-id="df177-105">A função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) permite que você defina, modifique, obtenha e remova pontos de nova análise.</span><span class="sxs-lookup"><span data-stu-id="df177-105">The [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function enables you to set, modify, obtain, and remove reparse points.</span></span> <span data-ttu-id="df177-106">A tabela a seguir descreve as operações de ponto de nova análise que você pode executar usando **DeviceIoControl**.</span><span class="sxs-lookup"><span data-stu-id="df177-106">The following table describes the reparse point operations that you can perform using **DeviceIoControl**.</span></span>



| <span data-ttu-id="df177-107">Operação</span><span class="sxs-lookup"><span data-stu-id="df177-107">Operation</span></span>                                                           | <span data-ttu-id="df177-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="df177-108">Description</span></span>                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df177-109">**FSCTL \_ definir \_ ponto de nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="df177-109">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | <span data-ttu-id="df177-110">Permite que o programa de chamada defina um novo ponto de nova análise ou modifique um existente.</span><span class="sxs-lookup"><span data-stu-id="df177-110">Allows the calling program to set a new reparse point, or to modify an existing one.</span></span><br/> |
| [<span data-ttu-id="df177-111">**FSCTL \_ obter \_ ponto de nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="df177-111">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | <span data-ttu-id="df177-112">Obtém as informações armazenadas em um ponto de nova análise existente.</span><span class="sxs-lookup"><span data-stu-id="df177-112">Obtains the information stored in an existing reparse point.</span></span><br/>                         |
| [<span data-ttu-id="df177-113">**FSCTL \_ excluir \_ ponto de nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="df177-113">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | <span data-ttu-id="df177-114">Remove um ponto de nova análise existente.</span><span class="sxs-lookup"><span data-stu-id="df177-114">Removes an existing reparse point.</span></span><br/>                                                   |



 

<span data-ttu-id="df177-115">Se você estiver modificando, obtendo ou excluindo um ponto de nova análise, deverá especificar a mesma marca de nova análise na operação contida no arquivo.</span><span class="sxs-lookup"><span data-stu-id="df177-115">If you are modifying, getting, or deleting a reparse point, you must specify the same reparse tag in the operation that is contained in the file.</span></span> <span data-ttu-id="df177-116">Caso contrário, a operação falhará com a **\_ \_ \_ incompatibilidade de erros de reanálise de erro** de erro.</span><span class="sxs-lookup"><span data-stu-id="df177-116">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_TAG\_MISMATCH**.</span></span> <span data-ttu-id="df177-117">Se você estiver modificando ou excluindo um ponto de nova análise, também deverá especificar o **GUID** de nova análise na operação contida no arquivo.</span><span class="sxs-lookup"><span data-stu-id="df177-117">If you are modifying or deleting a reparse point, you must also specify the reparse **GUID** in the operation that is contained in the file.</span></span> <span data-ttu-id="df177-118">Caso contrário, a operação falhará com o **erro de erro ao \_ reanalisar o \_ \_ conflito de atributo**.</span><span class="sxs-lookup"><span data-stu-id="df177-118">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**.</span></span>

<span data-ttu-id="df177-119">Para determinar se um arquivo ou diretório contém um ponto de nova análise, use a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="df177-119">To determine whether a file or directory contains a reparse point, use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function.</span></span> <span data-ttu-id="df177-120">Se o arquivo ou diretório tiver um ponto de nova análise associado, o atributo de **\_ \_ \_ ponto de nova análise de atributo de arquivo** será definido.</span><span class="sxs-lookup"><span data-stu-id="df177-120">If the file or directory has an associated reparse point, the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute is set.</span></span>

<span data-ttu-id="df177-121">Para substituir um ponto de nova análise existente sem que já tenha um identificador para o arquivo ou diretório, chame [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) com o **sinalizador de arquivo \_ \_ abrir \_ \_ ponto de nova análise**.</span><span class="sxs-lookup"><span data-stu-id="df177-121">To overwrite an existing reparse point without already having a handle to the file or directory, call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) with **FILE\_FLAG\_OPEN\_REPARSE\_POINT**.</span></span> <span data-ttu-id="df177-122">Esse sinalizador permite que você abra o arquivo se o filtro do sistema de arquivos correspondente está ou não instalado e funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="df177-122">This flag allows you to open the file whether or not the corresponding file system filter is installed and working correctly.</span></span>

 

