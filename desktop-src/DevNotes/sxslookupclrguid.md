---
description: Recupera o nome da classe e outras informações associadas a um determinado GUID no manifesto de um componente.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: Função SxsLookupClrGuid
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751348"
---
# <a name="sxslookupclrguid-function"></a><span data-ttu-id="ec743-103">Função SxsLookupClrGuid</span><span class="sxs-lookup"><span data-stu-id="ec743-103">SxsLookupClrGuid function</span></span>

<span data-ttu-id="ec743-104">Recupera o nome da classe e outras informações associadas a um determinado GUID no manifesto de um componente.</span><span class="sxs-lookup"><span data-stu-id="ec743-104">Retrieves the class name and other information associated with a given GUID in a component's manifest.</span></span> <span data-ttu-id="ec743-105">Essa função é usada somente ao implementar a interoperabilidade gerenciada e não gerenciada de baixo nível no .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ec743-105">This function is used only when implementing low-level managed-unmanaged interoperability in the .NET Framework.</span></span> <span data-ttu-id="ec743-106">Para obter mais informações sobre a interoperabilidade gerenciada não gerenciada, consulte "interoperação com código não gerenciado" no SDK do .NET Framework e também [aplicativos isolados e assemblies lado a lado](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ec743-106">For more information about managed-unmanaged interoperability, see "Interoperating with Unmanaged Code" in the .NET Framework SDK and also [Isolated Applications and Side-by-side Assemblies](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec743-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec743-107">Syntax</span></span>


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="ec743-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec743-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec743-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec743-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec743-110">Uma combinação de zero ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec743-110">A combination of zero or more of the following flags.</span></span>



| <span data-ttu-id="ec743-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ec743-111">Value</span></span>                                                                                                                                                                                                                                                                                             | <span data-ttu-id="ec743-112">Significado</span><span class="sxs-lookup"><span data-stu-id="ec743-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <span data-ttu-id="ec743-113"><dt>**SxS \_ Pesquisar \_ \_ GUID CLR \_ use \_ ACTCTX**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ec743-113"><dt>**SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX**</dt> <dt>0x00000001</dt></span></span> </dl>              | <span data-ttu-id="ec743-114">Se esse sinalizador for definido, o parâmetro *hActCtx* deverá conter um identificador de contexto de ativação retornado pela função [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="ec743-114">If this flag is set, then the *hActCtx* parameter must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="ec743-115">Se esse sinalizador não for definido, o parâmetro *hActCtx* será ignorado e **SxsLookupClrGuid** pesquisará o contexto de ativação que está ativo no momento (a função [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) é usada para tornar um contexto de ativação ativo).</span><span class="sxs-lookup"><span data-stu-id="ec743-115">If this flag is not set, the *hActCtx* parameter is ignored and **SxsLookupClrGuid** searches the activation context that is currently active (the [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) function is used to make an activation context active).</span></span><br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <span data-ttu-id="ec743-116"><dt>**SxS \_ Pesquisar \_ \_ GUID CLR \_ localizar \_**</dt> <dt>0x00010000</dt> substituto</span><span class="sxs-lookup"><span data-stu-id="ec743-116"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE**</dt> <dt>0x00010000</dt></span></span> </dl>  | <span data-ttu-id="ec743-117">Se esse sinalizador for definido, o **SxsLookupClrGuid** pesquisará um substituto.</span><span class="sxs-lookup"><span data-stu-id="ec743-117">If this flag is set, **SxsLookupClrGuid** searches for a surrogate.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <span data-ttu-id="ec743-118"><dt>**SxS \_ Pesquisar \_ \_ GUID CLR \_ localizar \_ \_ classe CLR**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="ec743-118"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="ec743-119">Se esse sinalizador for definido, **SxsLookupClrGuid** pesquisará uma classe.</span><span class="sxs-lookup"><span data-stu-id="ec743-119">If this flag is set, **SxsLookupClrGuid** searches for a class.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <span data-ttu-id="ec743-120"><dt>**SxS \_ Pesquisar \_ \_ GUID CLR \_ localizar \_ qualquer**</dt> <dt>0x00030000</dt></span><span class="sxs-lookup"><span data-stu-id="ec743-120"><dt>**SXS\_LOOKUP\_CLR\_GUID\_FIND\_ANY**</dt> <dt>0x00030000</dt></span></span> </dl>                    | <span data-ttu-id="ec743-121">Essa é uma combinação do **GUID de pesquisa de SxS de \_ \_ CRL \_ \_ localizar \_ substituto** e **SxS \_ pesquisador de CLR localizar sinalizadores de \_ \_ \_ \_ \_ classe CLR** ; se ambos estiverem definidos, **SxsLookupClrGuid** procurará um substituto primeiro e somente se ele não encontrar um, então procurará uma classe.</span><span class="sxs-lookup"><span data-stu-id="ec743-121">This is a combination of the **SXS\_LOOKUP\_CLR\_GUID\_FIND\_SURROGATE** and **SXS\_LOOKUP\_CLR\_GUID\_FIND\_CLR\_CLASS** flags; if both are set, **SxsLookupClrGuid** searches for a surrogate first, and only if it does not find one, then searches for a class.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="ec743-122">*pCLSID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec743-122">*pClsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec743-123">Um ponteiro para o GUID sobre o qual Pesquisar as informações de interoperação no contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="ec743-123">A pointer to the GUID about which to search the activation context for interoperation information.</span></span> <span data-ttu-id="ec743-124">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="ec743-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ec743-125">*hActCtx* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ec743-125">*hActCtx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec743-126">Se o **\_ GUID CLR de pesquisa de SxS \_ \_ \_ usar \_** o sinalizador ACTCTX estiver definido no parâmetro *dwFlags* , *hActCtx* deverá conter um identificador de contexto de ativação retornado pela função [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) .</span><span class="sxs-lookup"><span data-stu-id="ec743-126">If the **SXS\_LOOKUP\_CLR\_GUID\_USE\_ACTCTX** flag is set in the *dwFlags* parameter, then *hActCtx* must contain an activation-context handle returned by the [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) function.</span></span> <span data-ttu-id="ec743-127">Caso contrário, *hActCtx* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="ec743-127">Otherwise, *hActCtx* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="ec743-128">*pvOutputBuffer* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ec743-128">*pvOutputBuffer* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec743-129">Ponteiro para o buffer no qual as informações de retorno são copiadas.</span><span class="sxs-lookup"><span data-stu-id="ec743-129">Pointer to the buffer into which return information is copied.</span></span> <span data-ttu-id="ec743-130">Esse parâmetro pode ser de valor nulo somente se o parâmetro *cbOutputBuffer* tiver valor zero.</span><span class="sxs-lookup"><span data-stu-id="ec743-130">This parameter may be NULL-valued only if the *cbOutputBuffer* parameter is zero-valued.</span></span> <span data-ttu-id="ec743-131">Os dados colocados nesse buffer na saída (se houver) consistem em uma **estrutura \_ \_ \_ CLR de informações de GUID SxS** seguida por quaisquer dados de cadeia de caracteres adicionais necessários.</span><span class="sxs-lookup"><span data-stu-id="ec743-131">The data placed in this buffer on exit (if any) consists of a **SXS\_GUID\_INFORMATION\_CLR** structure followed by any additional string data required.</span></span> <span data-ttu-id="ec743-132">Consulte a seção comentários abaixo para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ec743-132">See the Remarks section below for more information.</span></span>

</dd> <dt>

<span data-ttu-id="ec743-133">*cbOutputBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec743-133">*cbOutputBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec743-134">Tamanho em bytes do buffer apontado pelo parâmetro *pvOutputBuffer* .</span><span class="sxs-lookup"><span data-stu-id="ec743-134">Size in bytes of the buffer pointed to by the *pvOutputBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ec743-135">*pcbOutputBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ec743-135">*pcbOutputBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec743-136">Ponteiro para uma variável em que o tamanho, em bytes, das informações de retorno é colocado na saída.</span><span class="sxs-lookup"><span data-stu-id="ec743-136">Pointer to a variable where the size, in bytes, of the return information is placed on exit.</span></span> <span data-ttu-id="ec743-137">Se o parâmetro *cbOutputBuffer* for zero ou se o tamanho do buffer de saída for menor do que o tamanho das informações de retorno, **SxsLookupClrGuid** falhará e [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de **\_ \_ buffer insuficiente**.</span><span class="sxs-lookup"><span data-stu-id="ec743-137">If the *cbOutputBuffer* parameter is zero, or if the size of the output buffer is smaller than the size of the return information, then **SxsLookupClrGuid** fails and [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns an error of **ERROR\_INSUFFICIENT\_BUFFER**.</span></span> <span data-ttu-id="ec743-138">Nesse caso, use o valor na variável apontada por *pcbOutputBuffer* para alocar um buffer grande o suficiente e, em seguida, chame **SxsLookupClrGuid** novamente para recuperar as informações desejadas.</span><span class="sxs-lookup"><span data-stu-id="ec743-138">In this case, use the value in the variable pointed to by *pcbOutputBuffer* to allocate a large enough buffer, and then call **SxsLookupClrGuid** again to retrieve the desired information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec743-139">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec743-139">Return value</span></span>

<span data-ttu-id="ec743-140">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ec743-140">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="ec743-141">Para obter mais informações de erro, chame [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span><span class="sxs-lookup"><span data-stu-id="ec743-141">For more error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)</span></span>

## <a name="remarks"></a><span data-ttu-id="ec743-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec743-142">Remarks</span></span>

<span data-ttu-id="ec743-143">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ec743-143">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="ec743-144">Os componentes gerenciados podem se declarar como suporte a "assemblies de interoperabilidade" gerenciados para permitir que um consumidor de componente Win32 não gerenciado referencie o assembly declarativo.</span><span class="sxs-lookup"><span data-stu-id="ec743-144">Managed components may declare themselves as supporting managed "interop assemblies" so as to allow an unmanaged Win32 component consumer to reference the declaring assembly.</span></span> <span data-ttu-id="ec743-145">O consumidor do componente pode interagir com o componente gerenciado chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em um GUID.</span><span class="sxs-lookup"><span data-stu-id="ec743-145">The component consumer can interact with the managed component by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) on a GUID.</span></span> <span data-ttu-id="ec743-146">A camada de interoperação roteia a solicitação de criação de objeto para .NET Framework, cria uma instância do objeto gerenciado e retorna um ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="ec743-146">The interoperation layer routes the object creation request to .NET Framework, creates an instance of the managed object, and returns an interface pointer.</span></span>

<span data-ttu-id="ec743-147">O **SxsLookupClrGuid** permite que as estruturas recuperem informações associadas a um determinado GUID no manifesto do componente, como o que é o nome da classe .net, qual versão do .NET Framework ela requer e em qual assembly host ele está localizado.</span><span class="sxs-lookup"><span data-stu-id="ec743-147">**SxsLookupClrGuid** allows the frameworks to retrieve information associated with a given GUID in the component's manifest, such as what its .NET class name is, what version of the .NET Framework it requires, and what host assembly it is located in.</span></span> <span data-ttu-id="ec743-148">Os componentes gerenciados publicam um assembly de interoperabilidade que contém várias instruções que associam GUIDs com nomes de assembly e de tipo, e os agentes de tempo de execução do .NET a construção de instâncias de objeto gerenciado quando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) é chamado.</span><span class="sxs-lookup"><span data-stu-id="ec743-148">Managed components publish an interop assembly that contains a number of statements associating GUIDs with assembly and type names, and the .NET runtime brokers the construction of managed object instances when [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is called.</span></span>

<span data-ttu-id="ec743-149">Veja a seguir um manifesto de componente de exemplo declarando um GUID CLR e um substituto CLR que o **SxsLookupClrGuid** pode Pesquisar:</span><span class="sxs-lookup"><span data-stu-id="ec743-149">The following is a sample component manifest declaring a CLR GUID and a CLR surrogate that **SxsLookupClrGuid** can look up:</span></span>

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

<span data-ttu-id="ec743-150">Um provedor de interoperação chamaria **SxsLookupClrGuid** com um ponteiro para o GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" e receberia, em seguida, retornará o nome de classe "MySampleSurrogate", a versão de tempo de execução necessária "1.0.3055" e a identidade textual "dotnet. Sample. substitutos, versão = ' 1.0.0.0 ', tipo = ' Interop '" do componente de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="ec743-150">An interoperation provider would call **SxsLookupClrGuid** with a pointer to the GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", and would receive in return the class name "MySampleSurrogate", the required runtime version "1.0.3055", and the textual identity "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" of the hosting component.</span></span>

<span data-ttu-id="ec743-151">Essas informações de retorno seriam contidas e/ou referenciadas por uma estrutura do **\_ CLR de \_ informações \_ de GUID SxS** declarada da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ec743-151">This return information would be contained and/or referenced by a **SXS\_GUID\_INFORMATION\_CLR** structure declared as follows.</span></span>

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

<span data-ttu-id="ec743-152">Os membros dessa estrutura contêm as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec743-152">The members of this structure contain the following information.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec743-153">Membro</span><span class="sxs-lookup"><span data-stu-id="ec743-153">Member</span></span></th>
<th><span data-ttu-id="ec743-154">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="ec743-154">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec743-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span><span class="sxs-lookup"><span data-stu-id="ec743-155"><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong></span></span><br/></td>
<td><span data-ttu-id="ec743-156">Contém o tamanho da estrutura de SXS_GUID_INFORMATION_CLR (isso permite que a estrutura cresça em versões posteriores).</span><span class="sxs-lookup"><span data-stu-id="ec743-156">Contains the size of the SXS_GUID_INFORMATION_CLR structure (this allows the structure to grow in later versions).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec743-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span><span class="sxs-lookup"><span data-stu-id="ec743-157"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong></span></span><br/></td>
<td><span data-ttu-id="ec743-158">Contém um dos dois valores de sinalizador a seguir:</span><span class="sxs-lookup"><span data-stu-id="ec743-158">Contains one of the following two flag values:</span></span> <br/>
<ul>
<li><span data-ttu-id="ec743-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): indica que o GUID especificado foi associado a um &quot; substituto.&quot;</span><span class="sxs-lookup"><span data-stu-id="ec743-159">SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): Indicates that the specified GUID was associated with a &quot;surrogate.&quot;</span></span></li>
<li><span data-ttu-id="ec743-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): indica que o GUID especificado foi associado a uma &quot; classe.&quot;</span><span class="sxs-lookup"><span data-stu-id="ec743-160">SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): Indicates that the specified GUID was associated with a &quot;class.&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec743-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span><span class="sxs-lookup"><span data-stu-id="ec743-161"><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong></span></span><br/></td>
<td><span data-ttu-id="ec743-162">Aponta para uma cadeia de caracteres largo com terminação zero que identifica a versão do tempo de execução especificado no manifesto do host para essa classe.</span><span class="sxs-lookup"><span data-stu-id="ec743-162">Points to a zero-terminated wide-character string that identifies the version of the runtime specified in the host manifest for this class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec743-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="ec743-163"><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong></span></span><br/></td>
<td><span data-ttu-id="ec743-164">Aponta para uma cadeia de caracteres largo com terminação zero que contém o nome da classe .NET associada ao GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="ec743-164">Points to a zero-terminated wide-character string that contains the name of the .NET class associated with the specified GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ec743-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span><span class="sxs-lookup"><span data-stu-id="ec743-165"><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong></span></span><br/></td>
<td><span data-ttu-id="ec743-166">Aponta para uma cadeia de caracteres largo com terminação zero que contém a identidade textual do assembly que hospeda essa classe.</span><span class="sxs-lookup"><span data-stu-id="ec743-166">Points to a zero-terminated wide-character string that contains the textual identity of the assembly that hosts this class.</span></span> <span data-ttu-id="ec743-167">Para obter mais informações sobre a identidade textual, consulte &quot; especificando nomes de tipos totalmente qualificados &quot; em &quot; descobrindo informações de tipo em tempo de execução &quot; em &quot; programação com o .NET Framework &quot; no SDK do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ec743-167">For more information about textual identity, see &quot;Specifying Fully Qualified Type Names&quot; under &quot;Discovering Type Information at Run Time&quot; under &quot;Programming with the .NET Framework&quot; in the .NET Framework SDK.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ec743-168">Um aplicativo não gerenciado pode usar as informações retornadas dessa maneira para carregar a versão correta do .NET Framework, carregar o assembly identificado pelo elemento **pcwszAssemblyIdentity** e, em seguida, criar uma instância da classe nomeada pelo elemento **pcwszTypeName** .</span><span class="sxs-lookup"><span data-stu-id="ec743-168">An unmanaged application can use the information returned in this fashion to load the right version of the .NET Framework, load the assembly identified by the **pcwszAssemblyIdentity** element, and then create an instance of the class named by the **pcwszTypeName** element.</span></span>

## <a name="examples"></a><span data-ttu-id="ec743-169">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ec743-169">Examples</span></span>

<span data-ttu-id="ec743-170">Use a vinculação dinâmica da seguinte maneira para chamar a função **SxsLookupClrGuid** :</span><span class="sxs-lookup"><span data-stu-id="ec743-170">Use dynamic linking as follows to call the **SxsLookupClrGuid** function:</span></span>


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a><span data-ttu-id="ec743-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec743-171">Requirements</span></span>



| <span data-ttu-id="ec743-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec743-172">Requirement</span></span> | <span data-ttu-id="ec743-173">Valor</span><span class="sxs-lookup"><span data-stu-id="ec743-173">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec743-174">DLL</span><span class="sxs-lookup"><span data-stu-id="ec743-174">DLL</span></span><br/> | <dl> <span data-ttu-id="ec743-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec743-175"><dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec743-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec743-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec743-177">Aplicativos isolados e assemblies lado a lado</span><span class="sxs-lookup"><span data-stu-id="ec743-177">Isolated Applications and Side-by-side Assemblies</span></span>](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[<span data-ttu-id="ec743-178">**CreateActCtx**</span><span class="sxs-lookup"><span data-stu-id="ec743-178">**CreateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[<span data-ttu-id="ec743-179">**ActivateActCtx**</span><span class="sxs-lookup"><span data-stu-id="ec743-179">**ActivateActCtx**</span></span>](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[<span data-ttu-id="ec743-180">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="ec743-180">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
