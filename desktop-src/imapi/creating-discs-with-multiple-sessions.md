---
title: Criando discos com várias sessões
description: O IMAPi é capaz de criar discos de dados de várias sessões. Há algumas considerações a serem consideradas ao criar um disco de várias sessões.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159653"
---
# <a name="creating-discs-with-multiple-sessions"></a><span data-ttu-id="873fc-104">Criando discos com várias sessões</span><span class="sxs-lookup"><span data-stu-id="873fc-104">Creating Discs with Multiple Sessions</span></span>

<span data-ttu-id="873fc-105">O IMAPi é capaz de criar discos de dados de várias sessões.</span><span class="sxs-lookup"><span data-stu-id="873fc-105">IMAPI is capable of creating multi-session data discs.</span></span> <span data-ttu-id="873fc-106">Há algumas considerações a serem consideradas ao criar um disco de várias sessões.</span><span class="sxs-lookup"><span data-stu-id="873fc-106">There are a few considerations to be aware of when creating a multi-session disc.</span></span>

<span data-ttu-id="873fc-107">O método [**IDiscMaster:: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina se há um disco IMAPI com várias sessões na unidade ativa na configuração.</span><span class="sxs-lookup"><span data-stu-id="873fc-107">The [**IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) method determines whether there is an IMAPI multi-session disc in the active drive upon setting.</span></span> <span data-ttu-id="873fc-108">Nesse caso, o IMAPi entra em modo de várias sessões automaticamente.</span><span class="sxs-lookup"><span data-stu-id="873fc-108">If so, IMAPI goes into multi-session mode automatically.</span></span> <span data-ttu-id="873fc-109">O uso de [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) após o modo de várias sessões ter sido estabelecido faz com que o IMAPI retorne ao modo de sessão única.</span><span class="sxs-lookup"><span data-stu-id="873fc-109">Using [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) after multi-session mode has been established causes IMAPI to return to single-session mode.</span></span> <span data-ttu-id="873fc-110">Isso significa que um disco em branco é necessário para uma gravação [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) .</span><span class="sxs-lookup"><span data-stu-id="873fc-110">This means that a blank disc is required for a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) burn.</span></span> <span data-ttu-id="873fc-111">Se o disco estiver no modo de várias sessões, o mesmo disco deverá estar no gravador ativo ou um código de erro de IMAPi \_ E \_ WRONGDISC será retornado.</span><span class="sxs-lookup"><span data-stu-id="873fc-111">If the disc is in multi-session mode, the same disc must be in the active recorder or an error code of IMAPI\_E\_WRONGDISC will be returned.</span></span>

<span data-ttu-id="873fc-112">A seleção de um gravador no formato Joliet faz com que o IMAPi Leia as informações do disco atualmente instalado. Se o disco for um disco de IMAPi Joliet anterior que tem espaço para outra sessão, o IMAPi se definirá automaticamente para o modo de várias sessões.</span><span class="sxs-lookup"><span data-stu-id="873fc-112">Selecting a recorder while in Joliet format causes IMAPI to read information from the currently installed disc. If the disc is a previous IMAPI Joliet disc that has space for another session, IMAPI automatically sets itself to multi-session mode.</span></span> <span data-ttu-id="873fc-113">Esse disco deve estar presente no gravador ativo ao chamar [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span><span class="sxs-lookup"><span data-stu-id="873fc-113">This disc must be present in the active recorder when calling [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span></span>

<span data-ttu-id="873fc-114">Fechar a primeira sessão em um disco requer 21 MB.</span><span class="sxs-lookup"><span data-stu-id="873fc-114">Closing the first session on a disc requires 21 MB.</span></span> <span data-ttu-id="873fc-115">Cada sessão adicional requer 11 MB para ser fechada.</span><span class="sxs-lookup"><span data-stu-id="873fc-115">Each additional session requires 11 MB to close.</span></span>

 

 




