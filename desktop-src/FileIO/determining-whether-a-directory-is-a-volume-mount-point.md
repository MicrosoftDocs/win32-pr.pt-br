---
description: Como determinar se um diretório especificado é uma pasta montada.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Determinando se um diretório é uma pasta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829678"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a><span data-ttu-id="b5964-103">Determinando se um diretório é uma pasta montada</span><span class="sxs-lookup"><span data-stu-id="b5964-103">Determining Whether a Directory Is a Mounted Folder</span></span>

<span data-ttu-id="b5964-104">É útil determinar se um diretório é uma pasta montada quando, por exemplo, você estiver usando um aplicativo de backup ou de pesquisa limitado a um volume.</span><span class="sxs-lookup"><span data-stu-id="b5964-104">It is useful to determine whether a directory is a mounted folder when, for example, you are using a backup or search application that is limited to one volume.</span></span> <span data-ttu-id="b5964-105">Esse aplicativo pode acessar informações em vários volumes se você usar funções como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para criar pastas montadas para os outros volumes no volume ao qual o aplicativo está limitado.</span><span class="sxs-lookup"><span data-stu-id="b5964-105">Such an application can reach information on multiple volumes if you use functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) to create mounted folders for the other volumes on the volume that the application is limited to.</span></span> <span data-ttu-id="b5964-106">Para obter mais informações, consulte [criando pastas montadas](mounting-and-dismounting-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="b5964-106">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>

<span data-ttu-id="b5964-107">Para determinar se um diretório especificado é uma pasta montada, primeiro chame a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) e inspecione o sinalizador de **\_ \_ \_ ponto de nova análise de atributo de arquivo** no valor de retorno para ver se o diretório tem um ponto de nova análise associado.</span><span class="sxs-lookup"><span data-stu-id="b5964-107">To determine if a specified directory is a mounted folder, first call the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function and inspect the **FILE\_ATTRIBUTE\_REPARSE\_POINT** flag in the return value to see if the directory has an associated reparse point.</span></span> <span data-ttu-id="b5964-108">Se tiver, use as funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) para obter a marca de nova análise no membro **dwReserved0** da estrutura de [**\_ \_ dados localizar do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="b5964-108">If it does, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions to obtain the reparse tag in the **dwReserved0** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="b5964-109">Para determinar se o ponto de nova análise é uma pasta montada (e não alguma outra forma de ponto de nova análise), teste se o valor da marca é igual ao valor de **\_ \_ \_ montagem da \_ marca de e/s**.</span><span class="sxs-lookup"><span data-stu-id="b5964-109">To determine if the reparse point is a mounted folder (and not some other form of reparse point), test whether the tag value equals the value **IO\_REPARSE\_TAG\_MOUNT\_POINT**.</span></span> <span data-ttu-id="b5964-110">Para obter mais informações, consulte [pontos de nova análise](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="b5964-110">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="b5964-111">Para obter o volume de destino de uma pasta montada, use a função [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="b5964-111">To obtain the target volume of a mounted folder, use the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>

<span data-ttu-id="b5964-112">De maneira semelhante, você pode determinar se um ponto de nova análise é um link simbólico testando se o valor da marca é **a \_ marca de Nova \_ análise \_ de e/s SYMLINK**.</span><span class="sxs-lookup"><span data-stu-id="b5964-112">In a similar manner, you can determine if a reparse point is a symbolic link by testing whether the tag value is **IO\_REPARSE\_TAG\_SYMLINK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5964-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5964-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5964-114">**Constantes de atributo de arquivo**</span><span class="sxs-lookup"><span data-stu-id="b5964-114">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 



