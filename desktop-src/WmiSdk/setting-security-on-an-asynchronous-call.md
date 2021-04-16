---
description: As chamadas assíncronas apresentam sérios riscos à segurança porque um retorno de chamada para o coletor pode não ser resultado da chamada assíncrona pelo aplicativo ou script original.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Definindo a segurança em uma chamada assíncrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761544"
---
# <a name="setting-security-on-an-asynchronous-call"></a><span data-ttu-id="21766-103">Definindo a segurança em uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="21766-103">Setting Security on an Asynchronous Call</span></span>

<span data-ttu-id="21766-104">As chamadas assíncronas apresentam sérios riscos à segurança porque um retorno de chamada para o [*coletor*](gloss-s.md) pode não ser resultado da chamada assíncrona pelo aplicativo ou script original.</span><span class="sxs-lookup"><span data-stu-id="21766-104">Asynchronous calls present serious security risks because a callback to the [*sink*](gloss-s.md) may not be a result of the asynchronous call by the original application or script.</span></span> <span data-ttu-id="21766-105">A segurança em conexões remotas é baseada na criptografia da comunicação entre o cliente e o provedor no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="21766-105">Security in remote connections is based on encryption of the communication between the client and the provider on the remote computer.</span></span> <span data-ttu-id="21766-106">No C++, você pode definir a criptografia por meio do parâmetro nível de autenticação na chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="21766-106">In C++ you can set encryption through the authentication level parameter in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="21766-107">Em script, defina o *AuthenticationLevel* na conexão do moniker ou em um objeto [**SWbemSecurity**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="21766-107">In scripting, set the *AuthenticationLevel* in the moniker connection or on an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="21766-108">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="21766-108">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="21766-109">Os riscos de segurança para chamadas assíncronas existem porque o WMI reduz o nível de autenticação em um retorno de chamada até que o retorno de chamada seja executado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="21766-109">The security risks for asynchronous calls exist because WMI lowers the authentication level on a callback until the callback succeeds.</span></span> <span data-ttu-id="21766-110">Em uma chamada assíncrona de saída, o cliente pode definir o nível de autenticação na conexão com o WMI.</span><span class="sxs-lookup"><span data-stu-id="21766-110">On an outgoing asynchronous call, the client can set the authentication level on the connection to WMI.</span></span> <span data-ttu-id="21766-111">O WMI recupera as configurações de segurança na chamada do cliente e tenta chamar de volta com o mesmo nível de autenticação.</span><span class="sxs-lookup"><span data-stu-id="21766-111">WMI retrieves the security settings on the client call and attempts to call back with the same authentication level.</span></span> <span data-ttu-id="21766-112">O retorno de chamada é sempre iniciado no nível de **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C** .</span><span class="sxs-lookup"><span data-stu-id="21766-112">The callback is always initiated at the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** level.</span></span> <span data-ttu-id="21766-113">Se o retorno de chamada falhar, o WMI reduzirá o nível de autenticação para um nível em que o retorno de chamada pode ter êxito, se necessário, para **RPC \_ C \_ Authn \_ nível \_ None**.</span><span class="sxs-lookup"><span data-stu-id="21766-113">If the callback fails, WMI lowers the authentication level to a level where the callback can succeed, if necessary, to **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span> <span data-ttu-id="21766-114">No contexto de chamadas no sistema local em que o serviço de autenticação não é Kerberos, o retorno de chamada é sempre retornado no **\_ \_ \_ nível \_ None do RPC C Authn**.</span><span class="sxs-lookup"><span data-stu-id="21766-114">In the context of calls within the local system where the authentication service is not Kerberos, the callback is always returned at **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span>

<span data-ttu-id="21766-115">O nível de autenticação mínimo é **RPC \_ C \_ Authn \_ nível \_ PKT** (**wbemAuthenticationLevelPkt** para scripting).</span><span class="sxs-lookup"><span data-stu-id="21766-115">The minimum authentication level is **RPC\_C\_AUTHN\_LEVEL\_PKT** (**wbemAuthenticationLevelPkt** for scripting).</span></span> <span data-ttu-id="21766-116">No entanto, você pode especificar um nível mais alto, como a **wbemAuthenticationLevelPktPrivacy**(privacidade do PCT de nível de autenticação) do **RPC \_ C \_ \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="21766-116">However, you can specify a higher level, such as **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="21766-117">É recomendável que os aplicativos cliente ou scripts definam o nível de autenticação para o padrão de **\_ \_ \_ nível \_** autentican do RPC C (**wbemAuthenticationLevelDefault**), que permite que o nível de autenticação seja negociado para o nível especificado pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="21766-117">It is recommended that client applications or scripts set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** (**wbemAuthenticationLevelDefault**) which allows the authentication level to be negotiated to the level specified by the server.</span></span>

<span data-ttu-id="21766-118">O valor do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controla se o WMI verifica um nível de autenticação aceitável em retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="21766-118">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level in callbacks.</span></span> <span data-ttu-id="21766-119">Esse é o único mecanismo para proteger a segurança do coletor para chamadas assíncronas feitas em scripts ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="21766-119">This is the only mechanism for protecting sink security for asynchronous calls made in scripting or Visual Basic.</span></span> <span data-ttu-id="21766-120">Por padrão, essa chave do registro é definida como zero.</span><span class="sxs-lookup"><span data-stu-id="21766-120">By default, this registry key is set to zero.</span></span> <span data-ttu-id="21766-121">Se a chave do registro for zero, o WMI não verificará os níveis de autenticação.</span><span class="sxs-lookup"><span data-stu-id="21766-121">If the registry key is zero then WMI does not verify authentication levels.</span></span> <span data-ttu-id="21766-122">Para proteger chamadas assíncronas em scripts, defina a chave do registro como 1.</span><span class="sxs-lookup"><span data-stu-id="21766-122">To secure asynchronous calls in scripting, set the registry key to 1.</span></span> <span data-ttu-id="21766-123">Os clientes C++ podem chamar [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) para controlar o acesso ao coletor.</span><span class="sxs-lookup"><span data-stu-id="21766-123">C++ clients can call [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) to control access to the sink.</span></span> <span data-ttu-id="21766-124">O valor é criado em qualquer lugar por padrão.</span><span class="sxs-lookup"><span data-stu-id="21766-124">The value is created anywhere by default.</span></span>

<span data-ttu-id="21766-125">Os tópicos a seguir fornecem exemplos de configuração de segurança de chamada assíncrona:</span><span class="sxs-lookup"><span data-stu-id="21766-125">The following topics provide examples of setting asynchronous call security:</span></span>

-   [<span data-ttu-id="21766-126">Definindo a segurança em uma chamada assíncrona no VBScript</span><span class="sxs-lookup"><span data-stu-id="21766-126">Setting Security on an Asynchronous Call in VBScript</span></span>](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   <span data-ttu-id="21766-127">Configurando a segurança de chamada assíncrona em C++</span><span class="sxs-lookup"><span data-stu-id="21766-127">Setting Asynchronous Call Security in C++</span></span>

## <a name="setting-asynchronous-call-security-in-c"></a><span data-ttu-id="21766-128">Configurando a segurança de chamada assíncrona em C++</span><span class="sxs-lookup"><span data-stu-id="21766-128">Setting Asynchronous Call Security in C++</span></span>

<span data-ttu-id="21766-129">O método [**IWbemUnsecuredApartment:: CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) é semelhante ao método [**IUnsecuredApartment:: CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) e cria um coletor em um processo separado, Unsecapp.exe, para receber retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="21766-129">The [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) method is similar to [**IUnsecuredApartment::CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) method and creates a sink in a separate process, Unsecapp.exe, to receive callbacks.</span></span> <span data-ttu-id="21766-130">No entanto, o método **CreateSinkStub** tem um parâmetro *dwFlag* que especifica como o processo separado manipula o controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="21766-130">However, the **CreateSinkStub** method has a *dwFlag* parameter that specifies how the separate process handles access control.</span></span>

<span data-ttu-id="21766-131">O parâmetro *dwFlag* especifica uma das seguintes ações para Unsecapp.exe:</span><span class="sxs-lookup"><span data-stu-id="21766-131">The *dwFlag* parameter specifies one of the following actions for Unsecapp.exe:</span></span>

-   <span data-ttu-id="21766-132">Use a configuração chave do registro para determinar se deseja ou não verificar o acesso.</span><span class="sxs-lookup"><span data-stu-id="21766-132">Use the registry key setting to determine whether or not to check access.</span></span>
-   <span data-ttu-id="21766-133">Ignore a chave do registro e sempre verifique o acesso.</span><span class="sxs-lookup"><span data-stu-id="21766-133">Ignore the registry key and always check access.</span></span>
-   <span data-ttu-id="21766-134">Ignore a chave do registro e nunca Verifique o acesso.</span><span class="sxs-lookup"><span data-stu-id="21766-134">Ignore the registry key and never check access.</span></span>

<span data-ttu-id="21766-135">O exemplo de código neste tópico requer a seguinte \# instrução include para compilação correta.</span><span class="sxs-lookup"><span data-stu-id="21766-135">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="21766-136">O procedimento a seguir descreve como executar uma chamada assíncrona com [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span><span class="sxs-lookup"><span data-stu-id="21766-136">The following procedure describes how to perform an asynchronous call with [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span></span>

<span data-ttu-id="21766-137">**Para executar uma chamada assíncrona com IWbemUnsecuredApartment**</span><span class="sxs-lookup"><span data-stu-id="21766-137">**To perform an asynchronous call with IWbemUnsecuredApartment**</span></span>

1.  <span data-ttu-id="21766-138">Crie um processo dedicado com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="21766-138">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="21766-139">O exemplo de código a seguir chama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar um processo dedicado.</span><span class="sxs-lookup"><span data-stu-id="21766-139">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
                     (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="21766-140">Crie uma instância do objeto Sink.</span><span class="sxs-lookup"><span data-stu-id="21766-140">Instantiate the sink object.</span></span>

    <span data-ttu-id="21766-141">O exemplo de código a seguir cria um novo objeto de coletor.</span><span class="sxs-lookup"><span data-stu-id="21766-141">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="21766-142">Crie um stub para o coletor.</span><span class="sxs-lookup"><span data-stu-id="21766-142">Create a stub for the sink.</span></span>

    <span data-ttu-id="21766-143">Um stub é uma função de wrapper produzida do coletor.</span><span class="sxs-lookup"><span data-stu-id="21766-143">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="21766-144">O exemplo de código a seguir cria um stub para o coletor.</span><span class="sxs-lookup"><span data-stu-id="21766-144">The following code example creates a stub for the sink.</span></span>

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  <span data-ttu-id="21766-145">Libere o ponteiro do objeto do coletor.</span><span class="sxs-lookup"><span data-stu-id="21766-145">Release the sink object pointer.</span></span>

    <span data-ttu-id="21766-146">Você pode liberar o ponteiro do objeto porque o stub agora possui o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="21766-146">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="21766-147">O exemplo de código a seguir libera o ponteiro do objeto.</span><span class="sxs-lookup"><span data-stu-id="21766-147">The following code example releases the object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

5.  <span data-ttu-id="21766-148">Use o stub em qualquer chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="21766-148">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="21766-149">Quando terminar com a chamada, libere a contagem de referência local.</span><span class="sxs-lookup"><span data-stu-id="21766-149">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="21766-150">O exemplo de código a seguir usa o stub em uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="21766-150">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="21766-151">Às vezes, talvez seja necessário cancelar uma chamada assíncrona depois de fazer a chamada.</span><span class="sxs-lookup"><span data-stu-id="21766-151">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="21766-152">Se você precisar cancelar a chamada, cancele a chamada com o mesmo ponteiro que originalmente fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="21766-152">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="21766-153">O exemplo de código a seguir descreve como cancelar uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="21766-153">The following code example describes how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  <span data-ttu-id="21766-154">Libere a contagem de referência local quando terminar de usar a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="21766-154">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="21766-155">Certifique-se de liberar o ponteiro *pStubSink* somente depois de confirmar que a chamada assíncrona não deve ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="21766-155">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not must be canceled.</span></span> <span data-ttu-id="21766-156">Além disso, não libere *pStubSink* depois que o WMI liberar o ponteiro do coletor *pSink* .</span><span class="sxs-lookup"><span data-stu-id="21766-156">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="21766-157">A liberação de *pStubSink* após o *pSink* cria uma contagem de referência circular na qual o coletor e o stub permanecem na memória para sempre.</span><span class="sxs-lookup"><span data-stu-id="21766-157">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="21766-158">Em vez disso, um local possível para liberar o ponteiro está na chamada [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) , feita pelo WMI para relatar que a chamada assíncrona original foi concluída.</span><span class="sxs-lookup"><span data-stu-id="21766-158">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

7.  <span data-ttu-id="21766-159">Quando terminar, não inicializar com com uma chamada para [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span><span class="sxs-lookup"><span data-stu-id="21766-159">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="21766-160">O exemplo de código a seguir mostra como chamar [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro *pUnsecApp* .</span><span class="sxs-lookup"><span data-stu-id="21766-160">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

<span data-ttu-id="21766-161">Para obter mais informações sobre a função [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) e os parâmetros, consulte a documentação [com](../cossdk/component-services-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="21766-161">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation.</span></span>

 

 
