---
description: Há um número de consultas interessantes em um driver que um aplicativo pode fazer se não houver nenhum custo de desempenho.
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: Notificação assíncrona (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771494"
---
# <a name="asynchronous-notification-direct3d-9"></a><span data-ttu-id="cff52-103">Notificação assíncrona (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cff52-103">Asynchronous Notification (Direct3D 9)</span></span>

<span data-ttu-id="cff52-104">Há um número de consultas interessantes em um driver que um aplicativo pode fazer se não houver nenhum custo de desempenho.</span><span class="sxs-lookup"><span data-stu-id="cff52-104">There are number of interesting queries on a driver that an application can make if there is no performance cost.</span></span> <span data-ttu-id="cff52-105">No Direct3D 7 e no Direct3D 8, um mecanismo de consulta síncrono, GetInfo, funcionou bem para coisas como estatísticas, mas nenhuma consulta de desempenho crítico foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="cff52-105">In Direct3D 7 and Direct3D 8, a synchronous query mechanism, GetInfo, worked well for things like statistics, but no performance-critical queries were added.</span></span> <span data-ttu-id="cff52-106">Há outras coisas (como limites) que são inerentemente assíncronas.</span><span class="sxs-lookup"><span data-stu-id="cff52-106">There are other things (like fences) that are inherently asynchronous.</span></span> <span data-ttu-id="cff52-107">Trata-se de uma API simples para fazer consultas síncronas.</span><span class="sxs-lookup"><span data-stu-id="cff52-107">This is a simple API to make both synchronous and asynchronous queries.</span></span> <span data-ttu-id="cff52-108">GetInfo será desativado no Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="cff52-108">GetInfo will be retired in Direct3D 9.</span></span>

<span data-ttu-id="cff52-109">Crie uma consulta usando [**IDirect3DDevice9:: CreateQuery**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="cff52-109">Create a query using [**IDirect3DDevice9::CreateQuery**](/windows/desktop/api).</span></span> <span data-ttu-id="cff52-110">Esse método usa um D3DQUERYTYPE, que define o tipo de consulta a ser feita e retorna um ponteiro para um objeto [**IDirect3DQuery9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="cff52-110">This method takes a D3DQUERYTYPE, which defines what kind of query to make and returns a pointer to an [**IDirect3DQuery9**](/windows/desktop/api) object.</span></span> <span data-ttu-id="cff52-111">Se não houver suporte para o tipo de consulta, a chamada retornará um erro D3DERR \_ não disponível.</span><span class="sxs-lookup"><span data-stu-id="cff52-111">If the query type is not supported, the call returns an error D3DERR\_NOTAVAILABLE.</span></span> <span data-ttu-id="cff52-112">Usando o objeto Query, o aplicativo envia a consulta para o tempo de execução usando [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)e sonda o status da consulta usando [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="cff52-112">Using the query object, the application submits the query to the runtime using [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue), and polls the query status using [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="cff52-113">Se o resultado da consulta estiver disponível, S \_ OK será retornado; caso contrário, \_ será retornado s false.</span><span class="sxs-lookup"><span data-stu-id="cff52-113">If the query result is available, S\_OK is returned; otherwise, S\_FALSE is returned.</span></span> <span data-ttu-id="cff52-114">Espera-se que o aplicativo passe um buffer de tamanho adequado para os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="cff52-114">The application is expected to pass an appropriately sized buffer for the query results.</span></span>

<span data-ttu-id="cff52-115">O aplicativo tem uma opção para forçar o tempo de execução para liberar a consulta para o driver usando D3DGETDATA \_ Flush com [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="cff52-115">The application has an option to force the runtime to flush the query down to the driver by using D3DGETDATA\_FLUSH with [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span> <span data-ttu-id="cff52-116">Isso causa uma liberação, forçando o driver a ver a consulta.</span><span class="sxs-lookup"><span data-stu-id="cff52-116">It causes a flush, forcing the driver to see the query.</span></span> <span data-ttu-id="cff52-117">Nesse caso, D3DERR \_ DEVICELOST será retornado se o dispositivo for perdido.</span><span class="sxs-lookup"><span data-stu-id="cff52-117">In this case, D3DERR\_DEVICELOST is returned if the device becomes lost.</span></span>

<span data-ttu-id="cff52-118">Todas as consultas são perdidas quando o dispositivo é perdido, o aplicativo precisa recriá-las.</span><span class="sxs-lookup"><span data-stu-id="cff52-118">All queries are lost when the device is lost, the application has to re-create them.</span></span> <span data-ttu-id="cff52-119">Se o dispositivo não oferecer suporte à consulta e o pQueryID for **nulo**, a criação da consulta falhará com D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cff52-119">If the device does not support the query and the pQueryID is **NULL**, the query creation will fail with D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="cff52-120">A tabela a seguir resume informações importantes sobre cada tipo de consulta.</span><span class="sxs-lookup"><span data-stu-id="cff52-120">The following table summaries important information about each query type.</span></span>



| <span data-ttu-id="cff52-121">QuertyType</span><span class="sxs-lookup"><span data-stu-id="cff52-121">QuertyType</span></span>                    | <span data-ttu-id="cff52-122">Sinalizador de problema válido</span><span class="sxs-lookup"><span data-stu-id="cff52-122">Valid issue flag</span></span>              | <span data-ttu-id="cff52-123">Buffer GetData</span><span class="sxs-lookup"><span data-stu-id="cff52-123">GetData buffer</span></span>              | <span data-ttu-id="cff52-124">Runtime</span><span class="sxs-lookup"><span data-stu-id="cff52-124">Runtime</span></span>      | <span data-ttu-id="cff52-125">Início implícito da consulta</span><span class="sxs-lookup"><span data-stu-id="cff52-125">Implicit beginning of query</span></span> |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| <span data-ttu-id="cff52-126">D3DQUERYTYPE \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="cff52-126">D3DQUERYTYPE\_VCACHE</span></span>          | <span data-ttu-id="cff52-127">D3DISSUE \_ fim</span><span class="sxs-lookup"><span data-stu-id="cff52-127">D3DISSUE\_END</span></span>                 | <span data-ttu-id="cff52-128">D3DDEVINFO \_ VCACHE</span><span class="sxs-lookup"><span data-stu-id="cff52-128">D3DDEVINFO\_VCACHE</span></span>          | <span data-ttu-id="cff52-129">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="cff52-129">Retail/Debug</span></span> | <span data-ttu-id="cff52-130">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="cff52-130">CreateDevice</span></span>                |
| <span data-ttu-id="cff52-131">\_RESOURCEMANAGER D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="cff52-131">D3DQUERYTYPE\_ResourceManager</span></span> | <span data-ttu-id="cff52-132">D3DISSUE \_ fim</span><span class="sxs-lookup"><span data-stu-id="cff52-132">D3DISSUE\_END</span></span>                 | <span data-ttu-id="cff52-133">\_RESOURCEMANAGER D3DDEVINFO</span><span class="sxs-lookup"><span data-stu-id="cff52-133">D3DDEVINFO\_ResourceManager</span></span> | <span data-ttu-id="cff52-134">Somente depuração</span><span class="sxs-lookup"><span data-stu-id="cff52-134">Debug only</span></span>   | <span data-ttu-id="cff52-135">Presente</span><span class="sxs-lookup"><span data-stu-id="cff52-135">Present</span></span>                     |
| <span data-ttu-id="cff52-136">D3DQUERYTYPE \_ VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="cff52-136">D3DQUERYTYPE\_VERTEXSTATS</span></span>     | <span data-ttu-id="cff52-137">D3DISSUE \_ fim</span><span class="sxs-lookup"><span data-stu-id="cff52-137">D3DISSUE\_END</span></span>                 | <span data-ttu-id="cff52-138">D3DDEVINFO \_ D3DVERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="cff52-138">D3DDEVINFO\_D3DVERTEXSTATS</span></span>  | <span data-ttu-id="cff52-139">Somente depuração</span><span class="sxs-lookup"><span data-stu-id="cff52-139">Debug only</span></span>   | <span data-ttu-id="cff52-140">Presente</span><span class="sxs-lookup"><span data-stu-id="cff52-140">Present</span></span>                     |
| <span data-ttu-id="cff52-141">\_Evento D3DQUERYTYPE</span><span class="sxs-lookup"><span data-stu-id="cff52-141">D3DQUERYTYPE\_EVENT</span></span>           | <span data-ttu-id="cff52-142">D3DISSUE \_ fim</span><span class="sxs-lookup"><span data-stu-id="cff52-142">D3DISSUE\_END</span></span>                 | <span data-ttu-id="cff52-143">BOOL</span><span class="sxs-lookup"><span data-stu-id="cff52-143">BOOL</span></span>                        | <span data-ttu-id="cff52-144">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="cff52-144">Retail/Debug</span></span> | <span data-ttu-id="cff52-145">CreateDevice</span><span class="sxs-lookup"><span data-stu-id="cff52-145">CreateDevice</span></span>                |
| <span data-ttu-id="cff52-146">D3DQUERYTYPE \_ oclusão</span><span class="sxs-lookup"><span data-stu-id="cff52-146">D3DQUERYTYPE\_OCCLUSION</span></span>       | <span data-ttu-id="cff52-147">Início do D3DISSUE \_ , \_ término do D3DISSUE</span><span class="sxs-lookup"><span data-stu-id="cff52-147">D3DISSUE\_BEGIN,D3DISSUE\_END</span></span> | <span data-ttu-id="cff52-148">DWORD</span><span class="sxs-lookup"><span data-stu-id="cff52-148">DWORD</span></span>                       | <span data-ttu-id="cff52-149">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="cff52-149">Retail/Debug</span></span> | <span data-ttu-id="cff52-150">N/D</span><span class="sxs-lookup"><span data-stu-id="cff52-150">N/A</span></span>                         |



 

<span data-ttu-id="cff52-151">Campo de sinalizadores para [**IDirect3DQuery9:: Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span><span class="sxs-lookup"><span data-stu-id="cff52-151">Flags field for [**IDirect3DQuery9::Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue):</span></span>


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



<span data-ttu-id="cff52-152">Campo de sinalizadores para [**IDirect3DQuery9:: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span><span class="sxs-lookup"><span data-stu-id="cff52-152">Flags field for [**IDirect3DQuery9::GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata):</span></span>


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a><span data-ttu-id="cff52-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cff52-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff52-154">Dicas de programação</span><span class="sxs-lookup"><span data-stu-id="cff52-154">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
