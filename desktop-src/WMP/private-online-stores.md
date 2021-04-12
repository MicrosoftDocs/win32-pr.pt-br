---
title: Lojas online privadas
description: Lojas online privadas
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Armazenamentos online do Windows Media Player, privado
- lojas online, privadas
- Digite 1 lojas online, privadas
- tipo 2 lojas online, privadas
- lojas online privadas
- registro, lojas online privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364187"
---
# <a name="private-online-stores"></a><span data-ttu-id="a0426-109">Lojas online privadas</span><span class="sxs-lookup"><span data-stu-id="a0426-109">Private Online Stores</span></span>

<span data-ttu-id="a0426-110">O Windows Media Player 10 ou posterior dá suporte a lojas online privadas; ou seja, os armazenamentos que são visíveis apenas para determinados usuários.</span><span class="sxs-lookup"><span data-stu-id="a0426-110">Windows Media Player 10 or later supports private online stores; that is, stores that are visible only to certain users.</span></span> <span data-ttu-id="a0426-111">Para que um repositório online privado fique visível para o usuário atual, deve haver uma entrada que represente a loja online privada na seguinte chave do registro.</span><span class="sxs-lookup"><span data-stu-id="a0426-111">For a private online store to be visible to the current user, there must be an entry that represents the private online store under the following registry key.</span></span>

<span data-ttu-id="a0426-112">HKEY \_ atual \_ software de usuário \\ \\ Microsoft \\ MediaPlayer \\ PrivateServices</span><span class="sxs-lookup"><span data-stu-id="a0426-112">HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\PrivateServices</span></span>

<span data-ttu-id="a0426-113">A entrada de registro necessária deve ter o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="a0426-113">The required registry entry must have the following format.</span></span>



| <span data-ttu-id="a0426-114">Nome</span><span class="sxs-lookup"><span data-stu-id="a0426-114">Name</span></span>                                                         | <span data-ttu-id="a0426-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0426-115">Type</span></span>           | <span data-ttu-id="a0426-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a0426-116">Value</span></span>                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="a0426-117">Qualquer nome escolhido pela pessoa que cria a entrada do registro</span><span class="sxs-lookup"><span data-stu-id="a0426-117">Any name chosen by the person who creates the registry entry</span></span> | <span data-ttu-id="a0426-118">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a0426-118">**REG\_DWORD**</span></span> | <span data-ttu-id="a0426-119">Um número, fornecido pela Microsoft, que identifica a loja online privada</span><span class="sxs-lookup"><span data-stu-id="a0426-119">A number, provided by Microsoft, that identifies the private online store</span></span> |



 

<span data-ttu-id="a0426-120">O controle ActiveX do Windows Media Player 10 dá suporte a lojas online privadas somente se o controle estiver sendo executado no modo remoto.</span><span class="sxs-lookup"><span data-stu-id="a0426-120">The Windows Media Player 10 ActiveX control supports private online stores only if the control is running in remote mode.</span></span> <span data-ttu-id="a0426-121">O controle ActiveX do Windows Media Player 11 dá suporte a lojas online privadas, independentemente de o controle estar sendo executado no modo remoto.</span><span class="sxs-lookup"><span data-stu-id="a0426-121">The Windows Media Player 11 ActiveX control supports private online stores regardless of whether the control is running in remote mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0426-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0426-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0426-123">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="a0426-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




