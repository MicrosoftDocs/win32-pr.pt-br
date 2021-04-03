---
description: Contém ponteiros para funções de retorno de chamada que podem ser usadas pelas funções do CSP (provedor de serviços de criptografia).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: Estrutura VTableProvStruc (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663141"
---
# <a name="vtableprovstruc-structure"></a><span data-ttu-id="d63a1-103">Estrutura VTableProvStruc</span><span class="sxs-lookup"><span data-stu-id="d63a1-103">VTableProvStruc structure</span></span>

<span data-ttu-id="d63a1-104">A estrutura **VTableProvStruc** contém ponteiros para funções de retorno de chamada que podem ser usadas pelas funções do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="d63a1-104">The **VTableProvStruc** structure contains pointers to callback functions that can be used by [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="d63a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d63a1-105">Syntax</span></span>


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a><span data-ttu-id="d63a1-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d63a1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d63a1-107">**Versão**</span><span class="sxs-lookup"><span data-stu-id="d63a1-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="d63a1-108">Um valor **DWORD** que indica a versão da estrutura.</span><span class="sxs-lookup"><span data-stu-id="d63a1-108">A **DWORD** value that indicates the version of the structure.</span></span> <span data-ttu-id="d63a1-109">Três versões desta estrutura são usadas.</span><span class="sxs-lookup"><span data-stu-id="d63a1-109">Three versions of this structure are used.</span></span> <span data-ttu-id="d63a1-110">As versões são número 1, 2 e 3 e determinam quais membros da estrutura são válidos.</span><span class="sxs-lookup"><span data-stu-id="d63a1-110">The versions are number 1, 2, and 3, and determine which members of the structure are valid.</span></span> <span data-ttu-id="d63a1-111">Os membros da versão 1 são válidos em todos os sistemas que dão suporte a essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="d63a1-111">Version 1 members are valid on all systems that support this structure.</span></span>

<span data-ttu-id="d63a1-112">Este é um membro da versão 1.</span><span class="sxs-lookup"><span data-stu-id="d63a1-112">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="d63a1-113">**FuncVerifyImage**</span><span class="sxs-lookup"><span data-stu-id="d63a1-113">**FuncVerifyImage**</span></span>
</dt> <dd>

<span data-ttu-id="d63a1-114">O endereço de uma função de retorno de chamada [**FuncVerifyImage**](funcverifyimage.md) que o CSP usa para verificar a assinatura de quaisquer DLLs que o CSP carregará.</span><span class="sxs-lookup"><span data-stu-id="d63a1-114">The address of a [**FuncVerifyImage**](funcverifyimage.md) callback function that the CSP uses to verify the signature of any DLLs that the CSP will load.</span></span> <span data-ttu-id="d63a1-115">Todas as DLLs auxiliares nas quais um CSP faz chamadas de função devem ser assinadas da mesma maneira (e com a mesma chave) que a DLL do CSP primário.</span><span class="sxs-lookup"><span data-stu-id="d63a1-115">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="d63a1-116">Para garantir essa assinatura, as DLLs auxiliares devem ser carregadas dinamicamente usando a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="d63a1-116">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="d63a1-117">Mas, antes que a DLL seja carregada, a assinatura da DLL deve ser verificada.</span><span class="sxs-lookup"><span data-stu-id="d63a1-117">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="d63a1-118">O CSP executa essa verificação chamando a função **FuncVerifyImage** , conforme mostrado no exemplo abaixo.</span><span class="sxs-lookup"><span data-stu-id="d63a1-118">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

<span data-ttu-id="d63a1-119">Esse ponteiro de função pode ser armazenado e usado até que o contexto do CSP seja liberado.</span><span class="sxs-lookup"><span data-stu-id="d63a1-119">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="d63a1-120">Este é um membro da versão 1.</span><span class="sxs-lookup"><span data-stu-id="d63a1-120">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="d63a1-121">**FuncReturnhWnd**</span><span class="sxs-lookup"><span data-stu-id="d63a1-121">**FuncReturnhWnd**</span></span>
</dt> <dd>

<span data-ttu-id="d63a1-122">O endereço de uma função de retorno de chamada [**FuncReturnhWnd**](funcreturnhwnd.md) que retorna o identificador de janela que o CSP deve usar como pai ou proprietário de qualquer interface do usuário que é exibida.</span><span class="sxs-lookup"><span data-stu-id="d63a1-122">The address of a [**FuncReturnhWnd**](funcreturnhwnd.md) callback function that returns the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span> <span data-ttu-id="d63a1-123">Os CSPs que não se comunicam diretamente com o usuário e os CSPs que usam hardware dedicado para essa finalidade podem ignorar essa entrada.</span><span class="sxs-lookup"><span data-stu-id="d63a1-123">CSPs that do not communicate directly with the user and CSPs that use dedicated hardware for this purpose can ignore this entry.</span></span> <span data-ttu-id="d63a1-124">Esse identificador de janela é zero por padrão, mas um aplicativo pode definir isso com um valor diferente usando a função [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) para definir a propriedade de **\_ \_ HWND de cliente PP** .</span><span class="sxs-lookup"><span data-stu-id="d63a1-124">This window handle is zero by default, but an application can set this to a different value by using the [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) function to set the **PP\_CLIENT\_HWND** property.</span></span>

<span data-ttu-id="d63a1-125">Esse ponteiro de função pode ser armazenado e usado até que o contexto do CSP seja liberado.</span><span class="sxs-lookup"><span data-stu-id="d63a1-125">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="d63a1-126">Este é um membro da versão 1.</span><span class="sxs-lookup"><span data-stu-id="d63a1-126">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="d63a1-127">**dwProvType**</span><span class="sxs-lookup"><span data-stu-id="d63a1-127">**dwProvType**</span></span>
</dt> <dd>

<span data-ttu-id="d63a1-128">Um valor **DWORD** que especifica o tipo de provedor a ser adquirido.</span><span class="sxs-lookup"><span data-stu-id="d63a1-128">A **DWORD** value that specifies the type of provider to acquire.</span></span> <span data-ttu-id="d63a1-129">Os seguintes [*tipos de provedor*](../secgloss/p-gly.md) são predefinidos e são discutidos em detalhes na [interoperabilidade do CSP](https://www.bing.com/search?q=CSP+Interoperability):</span><span class="sxs-lookup"><span data-stu-id="d63a1-129">The following [*provider types*](../secgloss/p-gly.md) are predefined and are discussed in detail in [CSP Interoperability](https://www.bing.com/search?q=CSP+Interoperability):</span></span>

-   <span data-ttu-id="d63a1-130">PROV \_ RSA \_ completo</span><span class="sxs-lookup"><span data-stu-id="d63a1-130">PROV\_RSA\_FULL</span></span>
-   <span data-ttu-id="d63a1-131">PROV \_ RSA \_ SIG</span><span class="sxs-lookup"><span data-stu-id="d63a1-131">PROV\_RSA\_SIG</span></span>
-   <span data-ttu-id="d63a1-132">PROV \_ DSS</span><span class="sxs-lookup"><span data-stu-id="d63a1-132">PROV\_DSS</span></span>
-   <span data-ttu-id="d63a1-133">PROV \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="d63a1-133">PROV\_FORTEZZA</span></span>
-   <span data-ttu-id="d63a1-134">PROV \_ MS \_ Exchange</span><span class="sxs-lookup"><span data-stu-id="d63a1-134">PROV\_MS\_EXCHANGE</span></span>

<span data-ttu-id="d63a1-135">Este é um membro da versão 2.</span><span class="sxs-lookup"><span data-stu-id="d63a1-135">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="d63a1-136">**pbContextInfo**</span><span class="sxs-lookup"><span data-stu-id="d63a1-136">**pbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d63a1-137">Um ponteiro para uma matriz de informações de contexto.</span><span class="sxs-lookup"><span data-stu-id="d63a1-137">A pointer to an array of context information.</span></span> <span data-ttu-id="d63a1-138">Os membros **pbContextInfo** e **cbContextInfo** juntos determinam o conjunto de informações usado quando uma função [**CPSETPROVPARAM**](https://www.bing.com/search?q=**CPSetProvParam**) é chamada com o PP do conjunto de \_ informações de contexto \_ .</span><span class="sxs-lookup"><span data-stu-id="d63a1-138">The **pbContextInfo** and **cbContextInfo** members together determine the information set used when a [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) function is called with PP\_CONTEXT\_INFO set.</span></span>

<span data-ttu-id="d63a1-139">Este é um membro da versão 2.</span><span class="sxs-lookup"><span data-stu-id="d63a1-139">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="d63a1-140">**cbContextInfo**</span><span class="sxs-lookup"><span data-stu-id="d63a1-140">**cbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="d63a1-141">Um valor **DWORD** que indica o número de elementos na matriz **pbContextInfo** .</span><span class="sxs-lookup"><span data-stu-id="d63a1-141">A **DWORD** value that indicates the number of elements in the **pbContextInfo** array.</span></span>

<span data-ttu-id="d63a1-142">Este é um membro da versão 2.</span><span class="sxs-lookup"><span data-stu-id="d63a1-142">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="d63a1-143">**pszProvName**</span><span class="sxs-lookup"><span data-stu-id="d63a1-143">**pszProvName**</span></span>
</dt> <dd>

<span data-ttu-id="d63a1-144">Uma cadeia de caracteres que contém o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="d63a1-144">A string that contains the name of the provider.</span></span>

<span data-ttu-id="d63a1-145">Este é um membro da versão 3.</span><span class="sxs-lookup"><span data-stu-id="d63a1-145">This is a version 3 member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d63a1-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="d63a1-146">Remarks</span></span>

<span data-ttu-id="d63a1-147">Os ponteiros na estrutura **VTableProvStruc** só estão disponíveis na função [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) .</span><span class="sxs-lookup"><span data-stu-id="d63a1-147">The pointers in the **VTableProvStruc** structure are only available within the [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) function.</span></span> <span data-ttu-id="d63a1-148">Se os membros da estrutura forem necessários depois que uma chamada para **CPAcquireContext** for concluída, as cópias dos elementos de estrutura necessários deverão ser feitas pelo CSP.</span><span class="sxs-lookup"><span data-stu-id="d63a1-148">If members of the structure are needed after a call to **CPAcquireContext** is completed, copies of the needed structure elements must be made by the CSP.</span></span> <span data-ttu-id="d63a1-149">Os ponteiros de função nessa estrutura podem ser armazenados e usados até que o contexto do CSP seja liberado.</span><span class="sxs-lookup"><span data-stu-id="d63a1-149">The function pointers in this structure can be stored and used until the CSP context is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63a1-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d63a1-150">Requirements</span></span>



| <span data-ttu-id="d63a1-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="d63a1-151">Requirement</span></span> | <span data-ttu-id="d63a1-152">Valor</span><span class="sxs-lookup"><span data-stu-id="d63a1-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d63a1-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d63a1-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d63a1-154">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d63a1-154">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d63a1-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d63a1-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d63a1-156">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d63a1-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d63a1-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d63a1-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="d63a1-158"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d63a1-158"><dt>Cspdk.h</dt></span></span> </dl> |
| <span data-ttu-id="d63a1-159">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d63a1-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d63a1-160">**VTableProvStrucW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="d63a1-160">**VTableProvStrucW** (Unicode)</span></span><br/>                                          |



 

 
