---
title: Recuperando o tipo de divisão de sequência
description: Recuperando o tipo de divisão de sequência
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- MIDI (interface digital de instrumento musical), tipo de divisão de sequência
- MIDI (interface digital de instrumento musical), tipo de divisão de sequência
- Sequenciador MIDI MCI, tipo de divisão
- MCI_STATUS comando
- tipo de divisão de sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6586a33fe4a5225fdcdca21e413104388d5831d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916222"
---
# <a name="retrieving-the-sequence-division-type"></a><span data-ttu-id="332f1-108">Recuperando o tipo de divisão de sequência</span><span class="sxs-lookup"><span data-stu-id="332f1-108">Retrieving the Sequence Division Type</span></span>

<span data-ttu-id="332f1-109">O *tipo de divisão* de uma sequência MIDI determina a quantidade de tempo entre os eventos de Midi na sequência.</span><span class="sxs-lookup"><span data-stu-id="332f1-109">The *division type* of a MIDI sequence determines the amount of time between MIDI events in the sequence.</span></span> <span data-ttu-id="332f1-110">Para determinar o tipo de divisão de uma sequência, use o comando [**\_ status do MCI**](mci-status.md) e defina o membro **dwItem** da estrutura de [**\_ \_ parâmetros do status do MCI**](mci-status-parms.md) como DIVTYPE do status do MCI \_ Seq \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="332f1-110">To determine the division type of a sequence, use the [**MCI\_STATUS**](mci-status.md) command and set the **dwItem** member of the [**MCI\_STATUS\_PARMS**](mci-status-parms.md) structure to MCI\_SEQ\_STATUS\_DIVTYPE .</span></span>

<span data-ttu-id="332f1-111">Se o **comando \_ status do MCI** for bem-sucedido, o membro **dwReturn** da **estrutura \_ \_ parâmetros do status do MCI** conterá um dos valores a seguir para indicar o tipo de divisão.</span><span class="sxs-lookup"><span data-stu-id="332f1-111">If the **MCI\_STATUS** command is successful, the **dwReturn** member of the **MCI\_STATUS\_PARMS** structure will contain one of the following values to indicate the division type.</span></span>



| <span data-ttu-id="332f1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="332f1-112">Value</span></span>                        | <span data-ttu-id="332f1-113">Tipo de divisão</span><span class="sxs-lookup"><span data-stu-id="332f1-113">Division type</span></span>                     |
|------------------------------|-----------------------------------|
| <span data-ttu-id="332f1-114">MCI \_ Seq \_ div \_ PPQN</span><span class="sxs-lookup"><span data-stu-id="332f1-114">MCI\_SEQ\_DIV\_PPQN</span></span>          | <span data-ttu-id="332f1-115">PPQN (observação de partes por trimestre)</span><span class="sxs-lookup"><span data-stu-id="332f1-115">PPQN (parts-per-quarter note)</span></span>     |
| <span data-ttu-id="332f1-116">MCI \_ Seq \_ div \_ SMPTE \_ 24</span><span class="sxs-lookup"><span data-stu-id="332f1-116">MCI\_SEQ\_DIV\_SMPTE\_24</span></span>     | <span data-ttu-id="332f1-117">SMPTE, 24 fps (quadros por segundo)</span><span class="sxs-lookup"><span data-stu-id="332f1-117">SMPTE, 24 fps (frames per second)</span></span> |
| <span data-ttu-id="332f1-118">MCI \_ Seq \_ div \_ SMPTE \_ 25</span><span class="sxs-lookup"><span data-stu-id="332f1-118">MCI\_SEQ\_DIV\_SMPTE\_25</span></span>     | <span data-ttu-id="332f1-119">SMPTE, 25 fps</span><span class="sxs-lookup"><span data-stu-id="332f1-119">SMPTE, 25 fps</span></span>                     |
| <span data-ttu-id="332f1-120">MCI \_ Seq \_ div \_ SMPTE \_ 30</span><span class="sxs-lookup"><span data-stu-id="332f1-120">MCI\_SEQ\_DIV\_SMPTE\_30</span></span>     | <span data-ttu-id="332f1-121">SMPTE, 30 fps</span><span class="sxs-lookup"><span data-stu-id="332f1-121">SMPTE, 30 fps</span></span>                     |
| <span data-ttu-id="332f1-122">MCI \_ Seq \_ div \_ SMPTE \_ 30DROP</span><span class="sxs-lookup"><span data-stu-id="332f1-122">MCI\_SEQ\_DIV\_SMPTE\_30DROP</span></span> | <span data-ttu-id="332f1-123">O quadro de soltar de SMPTE, 30 fps</span><span class="sxs-lookup"><span data-stu-id="332f1-123">SMPTE, 30 fps drop frame</span></span>          |



 

<span data-ttu-id="332f1-124">Você deve saber o tipo de divisão de uma sequência para alterar ou consultar seu tempo.</span><span class="sxs-lookup"><span data-stu-id="332f1-124">You must know the division type of a sequence to change or query its tempo.</span></span> <span data-ttu-id="332f1-125">Você não pode alterar o tipo de divisão de uma sequência usando o sequenciador MCI.</span><span class="sxs-lookup"><span data-stu-id="332f1-125">You cannot change the division type of a sequence by using the MCI sequencer.</span></span>

 

 




