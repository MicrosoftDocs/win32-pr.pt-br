---
title: Restauração de BITS e do sistema
description: Nem todas as versões de BITS usam o mesmo formato para armazenar trabalhos.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005058"
---
# <a name="bits-and-system-restore"></a><span data-ttu-id="c2b59-103">Restauração de BITS e do sistema</span><span class="sxs-lookup"><span data-stu-id="c2b59-103">BITS and System Restore</span></span>

<span data-ttu-id="c2b59-104">Nem todas as versões de BITS usam o mesmo formato para armazenar trabalhos.</span><span class="sxs-lookup"><span data-stu-id="c2b59-104">Not all versions of BITS use the same format to store jobs.</span></span> <span data-ttu-id="c2b59-105">Se você retornar o computador a um ponto de restauração antes de uma atualização do BITS, a versão antiga do BITS poderá não ser capaz de ler as informações do trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="c2b59-105">If you return the computer to a restore point prior to a BITS upgrade, the old version of BITS may not be able to read the current job information.</span></span> <span data-ttu-id="c2b59-106">Se isso acontecer, o BITS excluirá a lista de trabalhos e criará uma nova lista de trabalhos vazia.</span><span class="sxs-lookup"><span data-stu-id="c2b59-106">If this happens, BITS will delete the jobs list and create a new empty jobs list.</span></span> <span data-ttu-id="c2b59-107">Como resultado, os arquivos temporários associados à lista de trabalhos anteriores não são limpos; para recuperar o espaço em disco, você deve excluir os arquivos manualmente.</span><span class="sxs-lookup"><span data-stu-id="c2b59-107">As a result, the temporary files associated with the previous jobs list are not cleaned up; to reclaim the disk space, you must delete the files manually.</span></span>

<span data-ttu-id="c2b59-108">Os usuários familiarizados com a linha de comando do Windows podem evitar esse problema usando a [ferramenta BITSAdmin](bitsadmin-tool.md) para limpar a lista de trabalhos do bits antes de executar a restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="c2b59-108">Users familiar with the Windows command line can avoid this problem by using the [BITSAdmin tool](bitsadmin-tool.md) to clear the BITS jobs list before running System Restore.</span></span> <span data-ttu-id="c2b59-109">Para limpar a lista de trabalhos BITS, execute o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="c2b59-109">To clear the BITS jobs list, run the following command:</span></span>

<span data-ttu-id="c2b59-110">**Bitsadmin/Reset reiniciar/AllUsers**</span><span class="sxs-lookup"><span data-stu-id="c2b59-110">**bitsadmin /reset /allusers**</span></span>

<span data-ttu-id="c2b59-111">Observe que você deve ter privilégios de administrador para executar este comando.</span><span class="sxs-lookup"><span data-stu-id="c2b59-111">Note that you must have administrator privileges to run this command.</span></span>

 

 




