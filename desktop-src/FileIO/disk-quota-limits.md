---
description: Descreve dois tipos de limites de cota de disco e como os limites de cota de disco são medidos.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limites de cota de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757559"
---
# <a name="disk-quota-limits"></a><span data-ttu-id="f0e68-103">Limites de cota de disco</span><span class="sxs-lookup"><span data-stu-id="f0e68-103">Disk Quota Limits</span></span>

<span data-ttu-id="f0e68-104">O espaço em disco usado por cada arquivo é cobrado diretamente para o usuário que possui o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f0e68-104">The disk space that each file uses is charged directly to the user who owns the file.</span></span> <span data-ttu-id="f0e68-105">O proprietário de um arquivo é identificado pelo SID (identificador de segurança) nas informações de segurança do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f0e68-105">The owner of a file is identified by the security identifier (SID) in the security information for the file.</span></span> <span data-ttu-id="f0e68-106">O espaço total em disco cobrado para um usuário é a soma do comprimento de todos os fluxos de dados.</span><span class="sxs-lookup"><span data-stu-id="f0e68-106">The total disk space charged to a user is the sum of the length of all data streams.</span></span> <span data-ttu-id="f0e68-107">Em outras palavras, os fluxos de conjunto de propriedades e os fluxos de dados de usuários residentes afetam a cota do usuário.</span><span class="sxs-lookup"><span data-stu-id="f0e68-107">In other words, property set streams and resident user data streams affect the user's quota.</span></span>

<span data-ttu-id="f0e68-108">A cota não é cobrada por pontos de reanálise, descritores de segurança ou outros metadados associados aos arquivos.</span><span class="sxs-lookup"><span data-stu-id="f0e68-108">Quota is not charged for re-parse points, security descriptors, or other metadata that is associated with the files.</span></span> <span data-ttu-id="f0e68-109">A compactação ou descompactação de arquivos não afeta o espaço em disco relatado para os arquivos.</span><span class="sxs-lookup"><span data-stu-id="f0e68-109">Compressing or decompressing files does not affect the disk space reported for the files.</span></span> <span data-ttu-id="f0e68-110">Portanto, as configurações de cota em um volume podem ser comparadas com as configurações em outro volume.</span><span class="sxs-lookup"><span data-stu-id="f0e68-110">Therefore, quota settings on one volume can be compared to settings on another volume.</span></span>

<span data-ttu-id="f0e68-111">Há dois tipos de limites de cota de disco, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0e68-111">There are two types of disk quota limits, as shown in the following table.</span></span>



| <span data-ttu-id="f0e68-112">Limite</span><span class="sxs-lookup"><span data-stu-id="f0e68-112">Limit</span></span>                        | <span data-ttu-id="f0e68-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0e68-113">Description</span></span>                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e68-114">Limite de aviso</span><span class="sxs-lookup"><span data-stu-id="f0e68-114">Warning threshold</span></span><br/> | <span data-ttu-id="f0e68-115">Você pode configurar o sistema para gerar uma entrada de arquivo de log do sistema quando o espaço em disco cobrado para o usuário exceder esse valor.</span><span class="sxs-lookup"><span data-stu-id="f0e68-115">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="f0e68-116">Cota rígida</span><span class="sxs-lookup"><span data-stu-id="f0e68-116">Hard quota</span></span><br/>        | <span data-ttu-id="f0e68-117">Você pode configurar o sistema para gerar uma entrada de arquivo de log do sistema quando o espaço em disco cobrado para o usuário exceder esse valor.</span><span class="sxs-lookup"><span data-stu-id="f0e68-117">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span> <span data-ttu-id="f0e68-118">Você também pode configurar o sistema para negar espaço em disco adicional ao usuário quando o espaço em disco cobrado para o usuário exceder esse valor.</span><span class="sxs-lookup"><span data-stu-id="f0e68-118">You can also configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.</span></span><br/> |



 

<span data-ttu-id="f0e68-119">O sistema de arquivos NTFS cria automaticamente uma entrada de cota de usuário quando um usuário grava pela primeira vez no volume.</span><span class="sxs-lookup"><span data-stu-id="f0e68-119">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="f0e68-120">As entradas que são criadas automaticamente são atribuídas ao limite de aviso padrão e aos valores de limite de cota rígido para o volume.</span><span class="sxs-lookup"><span data-stu-id="f0e68-120">Entries that are created automatically are assigned the default warning threshold and hard quota limit values for the volume.</span></span>

 

 




