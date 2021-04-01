---
description: Esta seção descreve estruturas que você pode usar para desenvolver analisadores. Essas estruturas são usadas por funções que você pode usar para desenvolver analisadores e funções que você pode usar para desenvolver analisadores ou especialistas.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Estruturas do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922982"
---
# <a name="parser-structures"></a><span data-ttu-id="39d9b-104">Estruturas do analisador</span><span class="sxs-lookup"><span data-stu-id="39d9b-104">Parser Structures</span></span>

<span data-ttu-id="39d9b-105">Esta seção descreve estruturas que você pode usar para desenvolver analisadores.</span><span class="sxs-lookup"><span data-stu-id="39d9b-105">This section describes structures you can use to develop parsers.</span></span> <span data-ttu-id="39d9b-106">Essas estruturas são usadas por funções que você pode usar para desenvolver analisadores e funções que você pode usar para desenvolver analisadores ou especialistas.</span><span class="sxs-lookup"><span data-stu-id="39d9b-106">These structures are used by functions you can use to develop parsers and functions you can use to develop either parsers or experts.</span></span>



| <span data-ttu-id="39d9b-107">Estrutura</span><span class="sxs-lookup"><span data-stu-id="39d9b-107">Structure</span></span>                                 | <span data-ttu-id="39d9b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="39d9b-108">Description</span></span>                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39d9b-109">MACFRAME</span><span class="sxs-lookup"><span data-stu-id="39d9b-109">MACFRAME</span></span>](macframe.md)                  | <span data-ttu-id="39d9b-110">Define os protocolos iniciais mais comumente usados.</span><span class="sxs-lookup"><span data-stu-id="39d9b-110">Defines the most commonly used initial protocols.</span></span>                                                                               |
| [<span data-ttu-id="39d9b-111">ENTRYPOINTS</span><span class="sxs-lookup"><span data-stu-id="39d9b-111">ENTRYPOINTS</span></span>](entrypoints.md)            | <span data-ttu-id="39d9b-112">Especifica os ponteiros para os pontos de entrada para a DLL do analisador.</span><span class="sxs-lookup"><span data-stu-id="39d9b-112">Specifies pointers to the entry points for the Parser DLL.</span></span>                                                                      |
| [<span data-ttu-id="39d9b-113">FOLLOWENTRY de PF \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-113">PF\_FOLLOWENTRY</span></span>](pf-followentry.md)     | <span data-ttu-id="39d9b-114">Especifica o protocolo que segue o protocolo atual.</span><span class="sxs-lookup"><span data-stu-id="39d9b-114">Specifies the protocol that follows the current protocol.</span></span>                                                                       |
| [<span data-ttu-id="39d9b-115">seguir do PF \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-115">PF\_FOLLOWSET</span></span>](pf-followset.md)         | <span data-ttu-id="39d9b-116">Especifica o conjunto de protocolos que segue o protocolo atual.</span><span class="sxs-lookup"><span data-stu-id="39d9b-116">Specifies the set of protocols that follows the current protocol.</span></span>                                                               |
| [<span data-ttu-id="39d9b-117">HANDOFFENTRY de PF \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-117">PF\_HANDOFFENTRY</span></span>](pf-handoffentry.md)   | <span data-ttu-id="39d9b-118">Especifica o protocolo que passa para o protocolo atual ou o protocolo para o qual o protocolo atual é immãos.</span><span class="sxs-lookup"><span data-stu-id="39d9b-118">Specifies either the protocol that hands off to the current protocol or the protocol that the current protocol hands off to.</span></span>    |
| [<span data-ttu-id="39d9b-119">teleentregador de PF \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-119">PF\_HANDOFFSET</span></span>](pf-handoffset.md)       | <span data-ttu-id="39d9b-120">Especifica o conjunto de protocolos que são disponibilizados para o protocolo atual ou para o conjunto de protocolos que o protocolo atual transfere para o.</span><span class="sxs-lookup"><span data-stu-id="39d9b-120">Specifies the set of protocols that hand off to the current protocol or the set of protocols the current protocol hands off to.</span></span> |
| [<span data-ttu-id="39d9b-121">PARSERDLLINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-121">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md) | <span data-ttu-id="39d9b-122">Especifica o número de analisadores na DLL do analisador e informações sobre cada analisador.</span><span class="sxs-lookup"><span data-stu-id="39d9b-122">Specifies the number of parsers in the parser DLL and information about each parser.</span></span>                                            |
| [<span data-ttu-id="39d9b-123">PARSERINFO de PF \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-123">PF\_PARSERINFO</span></span>](pf-parserinfo.md)       | <span data-ttu-id="39d9b-124">Especifica informações sobre um analisador específico.</span><span class="sxs-lookup"><span data-stu-id="39d9b-124">Specifies information about a specific parser.</span></span>                                                                                  |
| [<span data-ttu-id="39d9b-125">BIT ROTULAdo \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-125">LABELED\_BIT</span></span>](labeled-bit.md)           | <span data-ttu-id="39d9b-126">Especifica identificadores, campos de bits ou sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="39d9b-126">Specifies handles, BIT fields, or flags.</span></span>                                                                                        |
| [<span data-ttu-id="39d9b-127">BYTE ROTULAdo \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-127">LABELED\_BYTE</span></span>](labeled-byte.md)         | <span data-ttu-id="39d9b-128">Especifica um par de rótulos de **byte** .</span><span class="sxs-lookup"><span data-stu-id="39d9b-128">Specifies a **BYTE** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="39d9b-129">RÓTULO \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="39d9b-129">LABELED\_DWORD</span></span>](labeled-dword.md)       | <span data-ttu-id="39d9b-130">Especifica um par de rótulos **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="39d9b-130">Specifies a **DWORD** label pair.</span></span>                                                                                               |
| [<span data-ttu-id="39d9b-131">palavra ROTULAda \_</span><span class="sxs-lookup"><span data-stu-id="39d9b-131">LABELED\_WORD</span></span>](labeled-word.md)         | <span data-ttu-id="39d9b-132">Especifica um par de rótulos de **palavras** .</span><span class="sxs-lookup"><span data-stu-id="39d9b-132">Specifies a **WORD** label pair.</span></span>                                                                                                |
| [<span data-ttu-id="39d9b-133">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="39d9b-133">PROPERTYINFO</span></span>](propertyinfo.md)          | <span data-ttu-id="39d9b-134">Especifica as propriedades que o analisador de protocolo requer para descrever os quadros.</span><span class="sxs-lookup"><span data-stu-id="39d9b-134">Specifies the properties that the protocol parser requires to describe frames.</span></span>                                                  |
| [<span data-ttu-id="39d9b-135">PROPERTYINST</span><span class="sxs-lookup"><span data-stu-id="39d9b-135">PROPERTYINST</span></span>](propertyinst.md)          | <span data-ttu-id="39d9b-136">Especifica uma instância de uma propriedade em um quadro.</span><span class="sxs-lookup"><span data-stu-id="39d9b-136">Specifies an instance of a property in a frame.</span></span>                                                                                 |
| [<span data-ttu-id="39d9b-137">PROPERTYINSTEX</span><span class="sxs-lookup"><span data-stu-id="39d9b-137">PROPERTYINSTEX</span></span>](propertyinstex.md)      | <span data-ttu-id="39d9b-138">Especifica uma instância de propriedade de forma livre e estendida.</span><span class="sxs-lookup"><span data-stu-id="39d9b-138">Specifies a free-form, extended property instance.</span></span>                                                                              |
| [<span data-ttu-id="39d9b-139">PROTOCOLINFO</span><span class="sxs-lookup"><span data-stu-id="39d9b-139">PROTOCOLINFO</span></span>](protocolinfo.md)          | <span data-ttu-id="39d9b-140">Especifica um protocolo.</span><span class="sxs-lookup"><span data-stu-id="39d9b-140">Specifies a protocol.</span></span>                                                                                                           |
| [<span data-ttu-id="39d9b-141">AMPLITUDE</span><span class="sxs-lookup"><span data-stu-id="39d9b-141">RANGE</span></span>](range.md)                        | <span data-ttu-id="39d9b-142">Especifica um intervalo para um número.</span><span class="sxs-lookup"><span data-stu-id="39d9b-142">Specifies a range for a number.</span></span>                                                                                                 |
| [<span data-ttu-id="39d9b-143">SET</span><span class="sxs-lookup"><span data-stu-id="39d9b-143">SET</span></span>](set.md)                            | <span data-ttu-id="39d9b-144">Especifica uma tabela de valores para uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="39d9b-144">Specifies a table of values for a property.</span></span>                                                                                     |



 

<span data-ttu-id="39d9b-145">Para obter informações sobre as funções usadas para desenvolver DLLs do analisador, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="39d9b-145">For information about functions used to develop parser DLLs, see the following topics.</span></span>



| <span data-ttu-id="39d9b-146">Para obter informações sobre</span><span class="sxs-lookup"><span data-stu-id="39d9b-146">For information about</span></span>                                         | <span data-ttu-id="39d9b-147">Consulte</span><span class="sxs-lookup"><span data-stu-id="39d9b-147">See</span></span>                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="39d9b-148">Funções que as DLLs do analisador exportam.</span><span class="sxs-lookup"><span data-stu-id="39d9b-148">Functions that the parser DLLs export.</span></span>                        | [<span data-ttu-id="39d9b-149">Funções de exportação de DLL do analisador</span><span class="sxs-lookup"><span data-stu-id="39d9b-149">Parser DLL Export Functions</span></span>](parser-dll-export-functions.md)               |
| <span data-ttu-id="39d9b-150">Funções que você pode usar para desenvolver DLLs do analisador.</span><span class="sxs-lookup"><span data-stu-id="39d9b-150">Functions that you can use to develop parser DLLs.</span></span>            | [<span data-ttu-id="39d9b-151">Funções do analisador</span><span class="sxs-lookup"><span data-stu-id="39d9b-151">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="39d9b-152">Funções que você pode usar para desenvolver DLLs de analisador e especialistas.</span><span class="sxs-lookup"><span data-stu-id="39d9b-152">Functions that you can use to develop parser and expert DLLs.</span></span> | [<span data-ttu-id="39d9b-153">Funções comuns de expert e parser</span><span class="sxs-lookup"><span data-stu-id="39d9b-153">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



