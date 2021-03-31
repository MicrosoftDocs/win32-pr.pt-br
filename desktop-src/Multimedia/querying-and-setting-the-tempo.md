---
title: Consultando e definindo o tempo
description: Consultando e definindo o tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- MIDI (interface digital de instrumento musical), tempo
- MIDI (interface digital de instrumentos musicais), tempo
- Sequenciador MIDI MCI, tempo
- MCI_STATUS comando
- tempo de sequência
- golpe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637261"
---
# <a name="querying-and-setting-the-tempo"></a><span data-ttu-id="29e99-109">Consultando e definindo o tempo</span><span class="sxs-lookup"><span data-stu-id="29e99-109">Querying and Setting the Tempo</span></span>

<span data-ttu-id="29e99-110">Para recuperar o tempo de uma sequência, use o [**comando \_ status do MCI**](mci-status.md) e defina o membro **dwItem** da estrutura de [**parâmetros do \_ status \_ do MCI**](mci-status-parms.md) para o \_ tempo de status de Seq MCI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="29e99-110">To retrieve the tempo of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_TEMPO.</span></span> <span data-ttu-id="29e99-111">Se o **comando \_ status do MCI** for bem-sucedido, o membro **dwReturn** da **estrutura \_ \_ parâmetros do status do MCI** conterá o tempo atual.</span><span class="sxs-lookup"><span data-stu-id="29e99-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure contains the current tempo.</span></span>

<span data-ttu-id="29e99-112">Para alterar o tempo, use o comando [**MCI \_ set**](mci-set.md) com a estrutura [**MCI \_ Seq \_ set \_ parms**](mci-seq-set-parms.md) , especificando o \_ sinalizador MCI Seq \_ set \_ tempo e definindo o membro **dwTempo** da estrutura para o tempo desejado.</span><span class="sxs-lookup"><span data-stu-id="29e99-112">To change tempo, use the [**MCI\_SET**](mci-set.md) command with the [**MCI\_SEQ\_SET\_PARMS**](mci-seq-set-parms.md) structure, specifying the MCI\_SEQ\_SET\_TEMPO flag and setting the **dwTempo** member of the structure to the desired tempo.</span></span>

<span data-ttu-id="29e99-113">A maneira como o tempo é representado depende do tipo de divisão da sequência.</span><span class="sxs-lookup"><span data-stu-id="29e99-113">The way tempo is represented depends on the division type of the sequence.</span></span> <span data-ttu-id="29e99-114">Se o tipo de divisão for PPQN, o tempo será representado em batidas por minuto.</span><span class="sxs-lookup"><span data-stu-id="29e99-114">If the division type is PPQN, the tempo is represented in beats per minute.</span></span> <span data-ttu-id="29e99-115">Se o tipo de divisão for um dos tipos de divisão SMPTE, o tempo será representado em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="29e99-115">If the division type is one of the SMPTE division types, the tempo is represented in frames per second.</span></span> <span data-ttu-id="29e99-116">Para obter informações sobre como determinar o tipo de divisão de uma sequência, consulte [recuperando o tipo de divisão de sequência](retrieving-the-sequence-division-type.md).</span><span class="sxs-lookup"><span data-stu-id="29e99-116">For information about determining the division type of a sequence, see [Retrieving the Sequence Division Type](retrieving-the-sequence-division-type.md).</span></span>

 

 




