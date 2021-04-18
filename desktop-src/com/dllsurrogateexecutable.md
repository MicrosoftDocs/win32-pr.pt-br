---
title: DllSurrogateExecutable
description: Permite que os servidores DLL sejam executados em um processo substituto personalizado, em conjunto com o valor do registro DllSurrogate. Se DllSurrogateExecutable não for especificado, COM passará NULL como o valor do primeiro parâmetro da função CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- COM valor do registro DllSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105764154"
---
# <a name="dllsurrogateexecutable"></a><span data-ttu-id="90d8e-105">DllSurrogateExecutable</span><span class="sxs-lookup"><span data-stu-id="90d8e-105">DllSurrogateExecutable</span></span>

<span data-ttu-id="90d8e-106">Permite que os servidores DLL sejam executados em um processo substituto personalizado, em conjunto com o valor do registro [**DllSurrogate**](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="90d8e-106">Enables DLL servers to run in a custom surrogate process, in conjunction with the [**DllSurrogate**](dllsurrogate.md) registry value.</span></span> <span data-ttu-id="90d8e-107">Se **DllSurrogateExecutable** não for especificado, com passará **NULL** como o valor do primeiro parâmetro da função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="90d8e-107">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="90d8e-108">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="90d8e-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a><span data-ttu-id="90d8e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="90d8e-109">Remarks</span></span>

<span data-ttu-id="90d8e-110">Esse valor é do tipo **reg \_ sz**.</span><span class="sxs-lookup"><span data-stu-id="90d8e-110">This value is of type **REG\_SZ**.</span></span> <span data-ttu-id="90d8e-111">Ele funciona em conjunto com o valor [**DllSurrogate**](dllsurrogate.md) para evitar qualquer ambiguidade ao usar a função [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="90d8e-111">It works in conjunction with the [**DllSurrogate**](dllsurrogate.md) value to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="90d8e-112">**DllSurrogate** indica se um substituto personalizado precisa ser usado e essas informações são passadas como o primeiro parâmetro para **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="90d8e-112">**DllSurrogate** indicates whether a custom surrogate needs to be used, and this information is passed as the first parameter for **CreateProcess**.</span></span> <span data-ttu-id="90d8e-113">Dependendo da implementação de **CreateProcess**, essas informações podem ser ambíguas.</span><span class="sxs-lookup"><span data-stu-id="90d8e-113">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="90d8e-114">Se **DllSurrogateExecutable** for especificado, com passará o valor como o primeiro parâmetro de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="90d8e-114">If **DllSurrogateExecutable** is specified, COM passes the value as the first parameter of **CreateProcess**.</span></span> <span data-ttu-id="90d8e-115">Se **DllSurrogateExecutable** não for especificado, com passará **NULL** como o valor para o primeiro parâmetro de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="90d8e-115">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90d8e-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90d8e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90d8e-117">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="90d8e-117">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="90d8e-118">Substitutos de DLL</span><span class="sxs-lookup"><span data-stu-id="90d8e-118">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="90d8e-119">**DllSurrogate**</span><span class="sxs-lookup"><span data-stu-id="90d8e-119">**DllSurrogate**</span></span>](dllsurrogate.md)
</dt> <dt>

[<span data-ttu-id="90d8e-120">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="90d8e-120">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 