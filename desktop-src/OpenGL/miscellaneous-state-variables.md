---
title: Variáveis de estado diversas
description: Variáveis de estado diversas
ms.assetid: 4c99b9b6-5cd3-49d1-9bfe-fa1421d892f2
keywords:
- Variáveis de estado variadas OpenGL
topic_type:
- apiref
api_name:
- Miscellaneous State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73da6292187fcbc9cd17f94fe88f63160d89be5b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638366"
---
# <a name="miscellaneous-state-variables"></a><span data-ttu-id="c5a64-104">Variáveis de estado diversas</span><span class="sxs-lookup"><span data-stu-id="c5a64-104">Miscellaneous State Variables</span></span>

<dl> <span data-ttu-id="c5a64-105"><dt><span id="GL_LIST_BASE"></span><span id="gl_list_base"></span>\_base da lista GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c5a64-105"><dt><span id="GL_LIST_BASE"></span><span id="gl_list_base"></span>GL\_LIST\_BASE</dt> </span></span><dd> 

|                  |                                        |
|------------------|----------------------------------------|
| <span data-ttu-id="c5a64-106">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c5a64-106">Description:</span></span>     | <span data-ttu-id="c5a64-107">Configuração de **glListBase**</span><span class="sxs-lookup"><span data-stu-id="c5a64-107">Setting of **glListBase**</span></span>              |
| <span data-ttu-id="c5a64-108">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c5a64-108">Attribute group:</span></span> | <span data-ttu-id="c5a64-109">list</span><span class="sxs-lookup"><span data-stu-id="c5a64-109">list</span></span>                                   |
| <span data-ttu-id="c5a64-110">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c5a64-110">Initial value:</span></span>   | <span data-ttu-id="c5a64-111">0</span><span class="sxs-lookup"><span data-stu-id="c5a64-111">0</span></span>                                      |
| <span data-ttu-id="c5a64-112">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c5a64-112">Get command:</span></span>     | [<span data-ttu-id="c5a64-113">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="c5a64-113">**glGetIntegerv**</span></span>](glgetintegerv.md) |



 

<span data-ttu-id="c5a64-114"></dd> <dt><span id="GL_LIST_INDEX"></span><span id="gl_list_index"></span>\_índice da lista GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c5a64-114"></dd> <dt><span id="GL_LIST_INDEX"></span><span id="gl_list_index"></span>GL\_LIST\_INDEX</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5a64-115">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c5a64-115">Description:</span></span>     | <span data-ttu-id="c5a64-116">Número de listas de exibição em construção; 0 se nenhum</span><span class="sxs-lookup"><span data-stu-id="c5a64-116">Number of display lists under construction; 0 if none</span></span>                            |
| <span data-ttu-id="c5a64-117">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c5a64-117">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="c5a64-118">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c5a64-118">Initial value:</span></span>   | <span data-ttu-id="c5a64-119">0</span><span class="sxs-lookup"><span data-stu-id="c5a64-119">0</span></span>                                                                                |
| <span data-ttu-id="c5a64-120">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c5a64-120">Get command:</span></span>     | [<span data-ttu-id="c5a64-121">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="c5a64-121">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c5a64-122"></dd> <dt><span id="GL_LIST_MODE"></span><span id="gl_list_mode"></span>\_modo de lista GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c5a64-122"></dd> <dt><span id="GL_LIST_MODE"></span><span id="gl_list_mode"></span>GL\_LIST\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5a64-123">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c5a64-123">Description:</span></span>     | <span data-ttu-id="c5a64-124">Modo de lista de exibição em construção; indefinido se nenhum</span><span class="sxs-lookup"><span data-stu-id="c5a64-124">Mode of display list under construction; undefined if none</span></span>                       |
| <span data-ttu-id="c5a64-125">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c5a64-125">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="c5a64-126">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c5a64-126">Initial value:</span></span>   | <span data-ttu-id="c5a64-127">0</span><span class="sxs-lookup"><span data-stu-id="c5a64-127">0</span></span>                                                                                |
| <span data-ttu-id="c5a64-128">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c5a64-128">Get command:</span></span>     | [<span data-ttu-id="c5a64-129">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="c5a64-129">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c5a64-130"></dd> <dt><span id="GL_ATTRIB_STACK_DEPTH"></span><span id="gl_attrib_stack_depth"></span>\_profundidade de \_ pilha de Atrib GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c5a64-130"></dd> <dt><span id="GL_ATTRIB_STACK_DEPTH"></span><span id="gl_attrib_stack_depth"></span>GL\_ATTRIB\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5a64-131">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c5a64-131">Description:</span></span>     | <span data-ttu-id="c5a64-132">Ponteiro de pilha de atributo</span><span class="sxs-lookup"><span data-stu-id="c5a64-132">Attribute stack pointer</span></span>                                                          |
| <span data-ttu-id="c5a64-133">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c5a64-133">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="c5a64-134">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c5a64-134">Initial value:</span></span>   | <span data-ttu-id="c5a64-135">0</span><span class="sxs-lookup"><span data-stu-id="c5a64-135">0</span></span>                                                                                |
| <span data-ttu-id="c5a64-136">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c5a64-136">Get command:</span></span>     | [<span data-ttu-id="c5a64-137">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="c5a64-137">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c5a64-138"></dd> <dt><span id="GL_NAME_STACK_DEPTH"></span><span id="gl_name_stack_depth"></span>\_profundidade da \_ pilha de nome GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c5a64-138"></dd> <dt><span id="GL_NAME_STACK_DEPTH"></span><span id="gl_name_stack_depth"></span>GL\_NAME\_STACK\_DEPTH</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5a64-139">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c5a64-139">Description:</span></span>     | <span data-ttu-id="c5a64-140">Profundidade da pilha de nomes</span><span class="sxs-lookup"><span data-stu-id="c5a64-140">Name stack depth</span></span>                                                                 |
| <span data-ttu-id="c5a64-141">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c5a64-141">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="c5a64-142">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c5a64-142">Initial value:</span></span>   | <span data-ttu-id="c5a64-143">0</span><span class="sxs-lookup"><span data-stu-id="c5a64-143">0</span></span>                                                                                |
| <span data-ttu-id="c5a64-144">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c5a64-144">Get command:</span></span>     | [<span data-ttu-id="c5a64-145">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="c5a64-145">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

<span data-ttu-id="c5a64-146"></dd> <dt><span id="GL_RENDER_MODE"></span><span id="gl_render_mode"></span>\_modo de RENDERIZAÇÃO GL \_</dt> </span><span class="sxs-lookup"><span data-stu-id="c5a64-146"></dd> <dt><span id="GL_RENDER_MODE"></span><span id="gl_render_mode"></span>GL\_RENDER\_MODE</dt> </span></span><dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5a64-147">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c5a64-147">Description:</span></span>     | <span data-ttu-id="c5a64-148">configuração de **glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="c5a64-148">**glRenderMode** setting</span></span>                                                         |
| <span data-ttu-id="c5a64-149">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c5a64-149">Attribute group:</span></span> |                                                                                  |
| <span data-ttu-id="c5a64-150">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c5a64-150">Initial value:</span></span>   | <span data-ttu-id="c5a64-151">\_RENDERIZAÇÃO GL</span><span class="sxs-lookup"><span data-stu-id="c5a64-151">GL\_RENDER</span></span>                                                                       |
| <span data-ttu-id="c5a64-152">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c5a64-152">Get command:</span></span>     | [<span data-ttu-id="c5a64-153">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="c5a64-153">**glGetIntegerv**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 



|                  |                                  |
|------------------|----------------------------------|
| <span data-ttu-id="c5a64-154">Descrição:</span><span class="sxs-lookup"><span data-stu-id="c5a64-154">Description:</span></span>     | <span data-ttu-id="c5a64-155">Códigos de erro atuais</span><span class="sxs-lookup"><span data-stu-id="c5a64-155">Current error codes</span></span>              |
| <span data-ttu-id="c5a64-156">Grupo de atributos:</span><span class="sxs-lookup"><span data-stu-id="c5a64-156">Attribute group:</span></span> |                                  |
| <span data-ttu-id="c5a64-157">Valor inicial:</span><span class="sxs-lookup"><span data-stu-id="c5a64-157">Initial value:</span></span>   | <span data-ttu-id="c5a64-158">0</span><span class="sxs-lookup"><span data-stu-id="c5a64-158">0</span></span>                                |
| <span data-ttu-id="c5a64-159">Comando Get:</span><span class="sxs-lookup"><span data-stu-id="c5a64-159">Get command:</span></span>     | [<span data-ttu-id="c5a64-160">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="c5a64-160">**glGetError**</span></span>](glgeterror.md) |



 

</dd> </dl>

 

 




