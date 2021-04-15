---
title: O moniker de elevação COM
description: O moniker de elevação COM permite que os aplicativos que estão sendo executados no controle de conta de usuário (UAC) ativem classes COM com privilégios elevados. Para obter mais informações, consulte concentre-se no privilégio mínimo.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454395"
---
# <a name="the-com-elevation-moniker"></a><span data-ttu-id="57af2-104">O moniker de elevação COM</span><span class="sxs-lookup"><span data-stu-id="57af2-104">The COM Elevation Moniker</span></span>

<span data-ttu-id="57af2-105">O moniker de elevação COM permite que os aplicativos que estão sendo executados no controle de conta de usuário (UAC) ativem classes COM com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="57af2-105">The COM elevation moniker allows applications that are running under user account control (UAC) to activate COM classes with elevated privileges.</span></span> <span data-ttu-id="57af2-106">Para obter mais informações, consulte [concentre-se no privilégio mínimo](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="57af2-106">For more information, see [Focus on Least Privilege](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span></span>

## <a name="when-to-use-the-elevation-moniker"></a><span data-ttu-id="57af2-107">Quando usar o moniker de elevação</span><span class="sxs-lookup"><span data-stu-id="57af2-107">When to Use the Elevation Moniker</span></span>

<span data-ttu-id="57af2-108">O moniker de elevação é usado para ativar uma classe COM para realizar uma função específica e limitada que exige privilégios elevados, como alterar a data e a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="57af2-108">The elevation moniker is used to activate a COM class to accomplish a specific and limited function that requires elevated privileges, such as changing the system date and time.</span></span>

<span data-ttu-id="57af2-109">A elevação requer a participação de uma classe COM e seu cliente.</span><span class="sxs-lookup"><span data-stu-id="57af2-109">Elevation requires participation from both a COM class and its client.</span></span> <span data-ttu-id="57af2-110">A classe COM deve ser configurada para dar suporte à elevação anotando sua entrada de registro, conforme descrito na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="57af2-110">The COM class must be configured to support elevation by annotating its registry entry, as described in the Requirements section.</span></span> <span data-ttu-id="57af2-111">O cliente COM deve solicitar elevação usando o moniker de elevação.</span><span class="sxs-lookup"><span data-stu-id="57af2-111">The COM client must request elevation by using the elevation moniker.</span></span>

<span data-ttu-id="57af2-112">O moniker de elevação não se destina a fornecer compatibilidade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="57af2-112">The elevation moniker is not intended to provide application compatibility.</span></span> <span data-ttu-id="57af2-113">Por exemplo, se você quiser executar um aplicativo COM herdado, como o WinWord como um servidor COM privilégios elevados, deverá configurar o executável do cliente COM para exigir elevação, em vez de ativar a classe do aplicativo herdado com o moniker de elevação.</span><span class="sxs-lookup"><span data-stu-id="57af2-113">For example, if you want to run a legacy COM application such as WinWord as an elevated server, you should configure the COM client executable to require elevation, rather than activating the legacy application's class with the elevation moniker.</span></span> <span data-ttu-id="57af2-114">Quando o cliente COM elevado chama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usando o CLSID do aplicativo herdado, o estado elevado do cliente flui para o processo do servidor.</span><span class="sxs-lookup"><span data-stu-id="57af2-114">When the elevated COM client calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) using the legacy application's CLSID, the client's elevated state will flow to the server process.</span></span>

<span data-ttu-id="57af2-115">Nem todas as funcionalidades COM são compatíveis com a elevação.</span><span class="sxs-lookup"><span data-stu-id="57af2-115">Not all COM functionality is compatible with elevation.</span></span> <span data-ttu-id="57af2-116">A funcionalidade que não funcionará inclui:</span><span class="sxs-lookup"><span data-stu-id="57af2-116">The functionality that will not work includes:</span></span>

-   <span data-ttu-id="57af2-117">A elevação não flui de um cliente para um servidor COM remoto.</span><span class="sxs-lookup"><span data-stu-id="57af2-117">Elevation does not flow from a client to a remote COM server.</span></span> <span data-ttu-id="57af2-118">Se um cliente ativar um servidor COM remoto com o moniker de elevação, o servidor não será elevado, mesmo que ele ofereça suporte à elevação.</span><span class="sxs-lookup"><span data-stu-id="57af2-118">If a client activates a remote COM server with the elevation moniker, the server will not be elevated, even if it supports elevation.</span></span>
-   <span data-ttu-id="57af2-119">Se uma classe COM privilegiada usar a representação durante uma chamada COM, poderá perder seus privilégios elevados durante a representação.</span><span class="sxs-lookup"><span data-stu-id="57af2-119">If an elevated COM class uses impersonation during a COM call, it might lose its elevated privileges during the impersonation.</span></span>
-   <span data-ttu-id="57af2-120">Se um servidor COM elevado registrar uma classe na corrompidos (tabela de objetos em execução), a classe não estará disponível para clientes não elevados.</span><span class="sxs-lookup"><span data-stu-id="57af2-120">If an elevated COM server registers a class in the running object table (ROT), the class will not be available to non-elevated clients.</span></span>
-   <span data-ttu-id="57af2-121">Um processo elevado usando o mecanismo UAC não carrega classes por usuário durante ativações COM.</span><span class="sxs-lookup"><span data-stu-id="57af2-121">A process elevated by using the UAC mechanism does not load per-user classes during COM activations.</span></span> <span data-ttu-id="57af2-122">Para aplicativos COM, isso significa que as classes COM do aplicativo devem ser instaladas no hive do registro do **\_ \_ computador local hKey** se o aplicativo for usado por contas sem privilégios e privilegiadas.</span><span class="sxs-lookup"><span data-stu-id="57af2-122">For COM applications, this means that the application's COM classes must be installed in the **HKEY\_LOCAL\_MACHINE** registry hive if the application is to be used both by non-privileged and privileged accounts.</span></span> <span data-ttu-id="57af2-123">As classes COM do aplicativo só precisam ser instaladas no hive de **\_ usuários do hKey** se o aplicativo nunca for usado por contas com privilégios.</span><span class="sxs-lookup"><span data-stu-id="57af2-123">The application's COM classes need only be installed in the **HKEY\_USERS** hive if the application is never used by privileged accounts.</span></span>
-   <span data-ttu-id="57af2-124">O recurso arrastar e soltar não é permitido de aplicativos não elevados para elevados.</span><span class="sxs-lookup"><span data-stu-id="57af2-124">Drag and drop is not allowed from non-elevated to elevated applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="57af2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57af2-125">Requirements</span></span>

<span data-ttu-id="57af2-126">Para usar o moniker de elevação para ativar uma classe COM, a classe deve ser configurada para ser executada como o usuário de inicialização ou a identidade de aplicativo ' Activate as Activator '.</span><span class="sxs-lookup"><span data-stu-id="57af2-126">In order to use the elevation moniker to activate a COM class, the class must be configured to run as the launching user or the 'Activate as Activator' application identity.</span></span> <span data-ttu-id="57af2-127">Se a classe estiver configurada para ser executada sob qualquer outra identidade, a ativação retornará o valor de erro de CO \_ E \_ runas \_ \_ deve \_ ser \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="57af2-127">If the class is configured to run under any other identity, the activation returns the error CO\_E\_RUNAS\_VALUE\_MUST\_BE\_AAA.</span></span>

<span data-ttu-id="57af2-128">A classe também deve ser anotada com um nome de exibição "amigável" que é compatível com MUI (Multilingual User interface).</span><span class="sxs-lookup"><span data-stu-id="57af2-128">The class must also be annotated with a "friendly" display name that is multilingual user interface (MUI) compatible.</span></span> <span data-ttu-id="57af2-129">Isso requer a seguinte entrada de registro:</span><span class="sxs-lookup"><span data-stu-id="57af2-129">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

<span data-ttu-id="57af2-130">Se essa entrada estiver ausente, a ativação retornará o erro CO \_ E \_ faltando \_ DISPLAYNAME.</span><span class="sxs-lookup"><span data-stu-id="57af2-130">If this entry is missing, the activation returns the error CO\_E\_MISSING\_DISPLAYNAME.</span></span> <span data-ttu-id="57af2-131">Se o arquivo MUI estiver ausente, o código de erro da função [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) será retornado.</span><span class="sxs-lookup"><span data-stu-id="57af2-131">If the MUI file is missing, the error code from the [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) function is returned.</span></span>

<span data-ttu-id="57af2-132">Opcionalmente, para especificar um ícone de aplicativo a ser exibido pela interface do usuário do UAC, adicione a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="57af2-132">Optionally, to specify an application icon to be displayed by the UAC user interface, add the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

<span data-ttu-id="57af2-133">**IconReference** usa o mesmo formato que a **localizadastring**:</span><span class="sxs-lookup"><span data-stu-id="57af2-133">**IconReference** uses the same format as **LocalizedString**:</span></span>

<span data-ttu-id="57af2-134">@*pathtobinary*,*-resourcenumber*</span><span class="sxs-lookup"><span data-stu-id="57af2-134">@*pathtobinary*,*-resourcenumber*</span></span>

<span data-ttu-id="57af2-135">Além disso, o componente COM deve ser assinado para que o ícone seja exibido.</span><span class="sxs-lookup"><span data-stu-id="57af2-135">In addition, the COM component must be signed for the icon to be displayed.</span></span>

<span data-ttu-id="57af2-136">A classe COM também deve ser anotada como habilitada para LUA.</span><span class="sxs-lookup"><span data-stu-id="57af2-136">The COM class must also be annotated as LUA-Enabled.</span></span> <span data-ttu-id="57af2-137">Isso requer a seguinte entrada de registro:</span><span class="sxs-lookup"><span data-stu-id="57af2-137">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

<span data-ttu-id="57af2-138">Se essa entrada estiver ausente, a ativação retornará o erro CO \_ E \_ elevação \_ desabilitada.</span><span class="sxs-lookup"><span data-stu-id="57af2-138">If this entry is missing, then the activation returns the error CO\_E\_ELEVATION\_DISABLED.</span></span>

<span data-ttu-id="57af2-139">Observe que essas entradas devem existir no hive do \_ computador local hKey \_ , não no \_ Hive HKEY Current \_ User ou HKEY \_ users.</span><span class="sxs-lookup"><span data-stu-id="57af2-139">Note that these entries must exist in the HKEY\_LOCAL\_MACHINE hive, not the HKEY\_CURRENT\_USER or HKEY\_USERS hive.</span></span> <span data-ttu-id="57af2-140">Isso impede que os usuários elevem classes COM que não tenham também os privilégios de registro.</span><span class="sxs-lookup"><span data-stu-id="57af2-140">This prevents users from elevating COM classes that they did not also have the privileges to register.</span></span>

## <a name="the-elevation-moniker-and-the-elevation-ui"></a><span data-ttu-id="57af2-141">O moniker de elevação e a interface do usuário de elevação</span><span class="sxs-lookup"><span data-stu-id="57af2-141">The Elevation Moniker and the Elevation UI</span></span>

<span data-ttu-id="57af2-142">Se o cliente já estiver elevado, usar o moniker de elevação não fará com que a interface do usuário de elevação seja exibida.</span><span class="sxs-lookup"><span data-stu-id="57af2-142">If the client is already elevated, using the elevation moniker will not cause the Elevation UI to display.</span></span>

## <a name="how-to-use-the-elevation-moniker"></a><span data-ttu-id="57af2-143">Como usar o moniker de elevação</span><span class="sxs-lookup"><span data-stu-id="57af2-143">How to Use the Elevation Moniker</span></span>

<span data-ttu-id="57af2-144">O moniker de elevação é um moniker COM padrão, semelhante aos monikers de sessão, partição ou fila.</span><span class="sxs-lookup"><span data-stu-id="57af2-144">The elevation moniker is a standard COM moniker, similar to the session, partition, or queue monikers.</span></span> <span data-ttu-id="57af2-145">Ele direciona uma solicitação de ativação para um servidor especificado com o nível de elevação especificado.</span><span class="sxs-lookup"><span data-stu-id="57af2-145">It directs an activation request to a specified server with the specified elevation level.</span></span> <span data-ttu-id="57af2-146">O CLSID a ser ativado aparece na cadeia de caracteres do moniker.</span><span class="sxs-lookup"><span data-stu-id="57af2-146">The CLSID to be activated appears in the moniker string.</span></span>

<span data-ttu-id="57af2-147">O moniker de elevação dá suporte aos seguintes tokens de nível de execução:</span><span class="sxs-lookup"><span data-stu-id="57af2-147">The elevation moniker supports the following Run level tokens:</span></span>

1.  <span data-ttu-id="57af2-148">Administrador</span><span class="sxs-lookup"><span data-stu-id="57af2-148">Administrator</span></span>
2.  <span data-ttu-id="57af2-149">O mais alto</span><span class="sxs-lookup"><span data-stu-id="57af2-149">Highest</span></span>

<span data-ttu-id="57af2-150">A sintaxe para isso é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="57af2-150">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

<span data-ttu-id="57af2-151">A sintaxe anterior usa o moniker "New" para retornar uma instância da classe COM especificada pelo *GUID*.</span><span class="sxs-lookup"><span data-stu-id="57af2-151">The preceding syntax uses the "new" moniker to return an instance of the COM class specified by *guid*.</span></span> <span data-ttu-id="57af2-152">Observe que o moniker "New" usa internamente a interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) para obter um objeto de classe e, em seguida, chama [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) nele.</span><span class="sxs-lookup"><span data-stu-id="57af2-152">Note that the "new" moniker internally uses the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface to obtain a class object and then calls [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) on it.</span></span>

<span data-ttu-id="57af2-153">O moniker de elevação também pode ser usado para obter um objeto de classe, que implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="57af2-153">The elevation moniker can also be used to get a class object, which implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="57af2-154">Em seguida, o chamador chama [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) para obter uma instância de objeto.</span><span class="sxs-lookup"><span data-stu-id="57af2-154">The caller then calls [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) to get an object instance.</span></span> <span data-ttu-id="57af2-155">A sintaxe para isso é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="57af2-155">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a><span data-ttu-id="57af2-156">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="57af2-156">Sample code</span></span>

<span data-ttu-id="57af2-157">O exemplo de código a seguir mostra como usar o moniker de elevação.</span><span class="sxs-lookup"><span data-stu-id="57af2-157">The following code example shows how to use the elevation moniker.</span></span> <span data-ttu-id="57af2-158">Ele pressupõe que você já tenha inicializado COM no thread atual.</span><span class="sxs-lookup"><span data-stu-id="57af2-158">It assumes that you have already initialized COM on the current thread.</span></span>


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



<span data-ttu-id="57af2-159">[**Associar \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) é novo no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="57af2-159">[**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) is new in Windows Vista.</span></span> <span data-ttu-id="57af2-160">Ele é derivado de [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span><span class="sxs-lookup"><span data-stu-id="57af2-160">It is derived from [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span></span>

<span data-ttu-id="57af2-161">A única adição é um campo **HWND** , **HWND**.</span><span class="sxs-lookup"><span data-stu-id="57af2-161">The only addition is an **HWND** field, **hwnd**.</span></span> <span data-ttu-id="57af2-162">Esse identificador representa uma janela que se torna o proprietário da interface do usuário de elevação, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="57af2-162">This handle represents a window that becomes the owner of the Elevation UI, if applicable.</span></span>

<span data-ttu-id="57af2-163">Se **HWND** for **NULL**, com chamará [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) para localizar um identificador de janela associado ao thread atual.</span><span class="sxs-lookup"><span data-stu-id="57af2-163">If **hwnd** is **NULL**, COM will call [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) to find a window handle associated with the current thread.</span></span> <span data-ttu-id="57af2-164">Esse caso pode ocorrer se o cliente for um script, que não pode preencher uma [**estrutura \_ OPTS3 do BIND**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) .</span><span class="sxs-lookup"><span data-stu-id="57af2-164">This case might occur if the client is a script, which cannot fill in a [**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) structure.</span></span> <span data-ttu-id="57af2-165">Nesse caso, COM tentará usar a janela associada ao thread de script.</span><span class="sxs-lookup"><span data-stu-id="57af2-165">In this case, COM will try to use the window associated with the script thread.</span></span>

## <a name="over-the-shoulder-ots-elevation"></a><span data-ttu-id="57af2-166">Elevação OTS (over-the-tiracolo)</span><span class="sxs-lookup"><span data-stu-id="57af2-166">Over-The-Shoulder (OTS) Elevation</span></span>

<span data-ttu-id="57af2-167">A elevação OTS (over-the-tiracolo) refere-se ao cenário no qual um cliente executa um servidor com com as credenciais de um administrador, em vez de sua própria.</span><span class="sxs-lookup"><span data-stu-id="57af2-167">Over-the-shoulder (OTS) elevation refers to the scenario in which a client runs a COM server with an administrator's credentials rather than his or her own.</span></span> <span data-ttu-id="57af2-168">(O termo "ao longo do ressalto" significa que o administrador está observando o ressalto do cliente enquanto o cliente executa o servidor.)</span><span class="sxs-lookup"><span data-stu-id="57af2-168">(The term "over the shoulder" means that the administrator is watching over the client's shoulder as the client runs the server.)</span></span>

<span data-ttu-id="57af2-169">Esse cenário pode causar um problema para chamadas COM no servidor, porque o servidor pode não chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitamente (ou seja, de forma programática) ou implicitamente (ou seja, declarativamente, usando o registro).</span><span class="sxs-lookup"><span data-stu-id="57af2-169">This scenario might cause a problem for COM calls into the server, because the server might not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) either explicitly (that is, programmatically) or implicitly (that is, declaratively, using the registry).</span></span> <span data-ttu-id="57af2-170">Para esses servidores, COM computa um descritor de segurança que permite que somente administradores de si, de sistema e internos façam \\ chamadas com no servidor.</span><span class="sxs-lookup"><span data-stu-id="57af2-170">For such servers, COM computes a security descriptor that allows only SELF, SYSTEM, and Builtin\\Administrators to makes COM calls into the server.</span></span> <span data-ttu-id="57af2-171">Essa organização não funcionará em cenários OTS.</span><span class="sxs-lookup"><span data-stu-id="57af2-171">This arrangement will not work in OTS scenarios.</span></span> <span data-ttu-id="57af2-172">Em vez disso, o servidor deve chamar **CoInitializeSecurity**, explicitamente ou implicitamente, e especificar uma ACL que inclua o SID do grupo interativo e o System.</span><span class="sxs-lookup"><span data-stu-id="57af2-172">Instead, the server must call **CoInitializeSecurity**, either explicitly or implicitly, and specify an ACL that includes the INTERACTIVE group SID and SYSTEM.</span></span>

<span data-ttu-id="57af2-173">O exemplo de código a seguir mostra como criar um descritor de segurança (SD) com o SID do grupo interativo.</span><span class="sxs-lookup"><span data-stu-id="57af2-173">The following code example shows how to create a security descriptor (SD) with the INTERACTIVE group SID.</span></span>

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

<span data-ttu-id="57af2-174">O exemplo de código a seguir mostra como chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitamente com o SD do exemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="57af2-174">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitly with the SD from the previous code example:</span></span>


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



<span data-ttu-id="57af2-175">O exemplo de código a seguir mostra como chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitamente com o SD acima:</span><span class="sxs-lookup"><span data-stu-id="57af2-175">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitly with the above SD:</span></span>


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a><span data-ttu-id="57af2-176">Permissões COM e rótulos de acesso obrigatórios</span><span class="sxs-lookup"><span data-stu-id="57af2-176">COM Permissions and Mandatory Access Labels</span></span>

<span data-ttu-id="57af2-177">O Windows Vista apresenta a noção de *Rótulos de acesso obrigatórios* em descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="57af2-177">Windows Vista introduces the notion of *mandatory access labels* in security descriptors.</span></span> <span data-ttu-id="57af2-178">O rótulo determina se os clientes podem obter acesso de execução a um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="57af2-178">The label dictates whether clients can get execute access to a COM object.</span></span> <span data-ttu-id="57af2-179">O rótulo é especificado na parte SACL (lista de controle de acesso) do sistema do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="57af2-179">The label is specified in the system access control list (SACL) portion of the security descriptor.</span></span> <span data-ttu-id="57af2-180">No Windows Vista, o COM dá suporte ao \_ rótulo obrigatório do sistema \_ \_ nenhum \_ \_ rótulo de execução.</span><span class="sxs-lookup"><span data-stu-id="57af2-180">In Windows Vista, COM supports the SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP label.</span></span> <span data-ttu-id="57af2-181">As SACLs nas permissões COM são ignoradas em sistemas operacionais anteriores ao Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="57af2-181">SACLs in the COM permissions are ignored on operating systems prior to Windows Vista.</span></span>

<span data-ttu-id="57af2-182">A partir do Windows Vista, dcomcnfg.exe não dá suporte à alteração do nível de integridade (IL) em permissões COM.</span><span class="sxs-lookup"><span data-stu-id="57af2-182">As of Windows Vista, dcomcnfg.exe does not support changing the integrity level (IL) in COM permissions.</span></span> <span data-ttu-id="57af2-183">Ele deve ser definido programaticamente.</span><span class="sxs-lookup"><span data-stu-id="57af2-183">It must be set programmatically.</span></span>

<span data-ttu-id="57af2-184">O exemplo de código a seguir mostra como criar um descritor de segurança com um rótulo que permite solicitações de inicialização/ativação de todos os clientes de IL baixo.</span><span class="sxs-lookup"><span data-stu-id="57af2-184">The following code example shows how to create a COM security descriptor with a label that allows launch/activation requests from all LOW IL clients.</span></span> <span data-ttu-id="57af2-185">Observe que os rótulos são válidos para permissões de inicialização/ativação e chamada.</span><span class="sxs-lookup"><span data-stu-id="57af2-185">Note that the labels are valid for Launch/Activation and Call permissions.</span></span> <span data-ttu-id="57af2-186">Portanto, é possível gravar um servidor COM que não permita inicialização, ativação ou chamadas de clientes com um determinado IL.</span><span class="sxs-lookup"><span data-stu-id="57af2-186">Thus, it is possible to write a COM server that disallows launch, activation or calls from clients with a certain IL.</span></span> <span data-ttu-id="57af2-187">Para obter mais informações sobre os níveis de integridade, consulte a seção "entendendo o mecanismo de integridade do Windows Vista" em [compreendendo e trabalhando no modo protegido do Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="57af2-187">For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span></span>


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a><span data-ttu-id="57af2-188">Níveis de CoCreateInstance e integridade</span><span class="sxs-lookup"><span data-stu-id="57af2-188">CoCreateInstance and Integrity Levels</span></span>

<span data-ttu-id="57af2-189">O comportamento de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) foi alterado no Windows Vista, para evitar que clientes de Il baixo sejam vinculados a servidores com por padrão.</span><span class="sxs-lookup"><span data-stu-id="57af2-189">The behavior of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) has changed in Windows Vista, to prevent Low IL clients from binding to COM servers by default.</span></span> <span data-ttu-id="57af2-190">O servidor deve permitir explicitamente essas associações especificando a SACL.</span><span class="sxs-lookup"><span data-stu-id="57af2-190">The server must explicitly allow such bindings by specifying the SACL.</span></span> <span data-ttu-id="57af2-191">As alterações em **CoCreateInstance** são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="57af2-191">The changes to **CoCreateInstance** are as follows:</span></span>

1.  <span data-ttu-id="57af2-192">Ao iniciar um processo de servidor COM, o IL no token de processo do servidor é definido como o IL do token do cliente ou do servidor, o que for menor.</span><span class="sxs-lookup"><span data-stu-id="57af2-192">When launching a COM server process, the IL in the server process token is set to the client or server token IL, whichever is lower.</span></span>
2.  <span data-ttu-id="57af2-193">Por padrão, o COM impedirá que clientes de IL baixo se vinculem às instâncias em execução de qualquer servidor COM.</span><span class="sxs-lookup"><span data-stu-id="57af2-193">By default, COM will prevent Low IL clients from binding to running instances of any COM servers.</span></span> <span data-ttu-id="57af2-194">Para permitir a associação, o descritor de segurança de inicialização/ativação do servidor COM deve conter uma SACL que especifica o rótulo de IL baixo (consulte a seção anterior do código de exemplo para criar um descritor de segurança desse tipo).</span><span class="sxs-lookup"><span data-stu-id="57af2-194">To allow the bind, a COM server's Launch/Activation security descriptor must contain a SACL that specifies the Low IL label (see the previous section for the sample code to create such a security descriptor).</span></span>

## <a name="elevated-servers-and-rot-registrations"></a><span data-ttu-id="57af2-195">Servidores elevados e registros corrompidos</span><span class="sxs-lookup"><span data-stu-id="57af2-195">Elevated Servers and ROT Registrations</span></span>

<span data-ttu-id="57af2-196">Se um servidor COM quiser se registrar na corrompidos (tabela de objetos em execução) e permitir que qualquer cliente acesse o registro, ele deverá usar o \_ sinalizador ROTFLAGS ALLOWANYCLIENT.</span><span class="sxs-lookup"><span data-stu-id="57af2-196">If a COM server wishes to register in the running object table (ROT) and allow any client to access the registration, it must use the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="57af2-197">Um servidor COM "Activate as Activator" não pode especificar ROTFLAGS \_ ALLOWANYCLIENT porque o DCOMSCM (Gerenciador de controle de serviço) do DCOM impõe uma verificação de falsificação nesse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="57af2-197">An "Activate As Activator" COM server cannot specify ROTFLAGS\_ALLOWANYCLIENT because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="57af2-198">Portanto, no Windows Vista, COM adiciona suporte para uma nova entrada de registro que permite ao servidor estipular que seus registros CORROMPIDOSs serão disponibilizados para qualquer cliente:</span><span class="sxs-lookup"><span data-stu-id="57af2-198">Therefore, in Windows Vista, COM adds support for a new registry entry that allows the server to stipulate that its ROT registrations be made available to any client:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

<span data-ttu-id="57af2-199">O único valor válido para essa \_ entrada reg DWORD é:</span><span class="sxs-lookup"><span data-stu-id="57af2-199">The only valid value for this REG\_DWORD entry is:</span></span>

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

<span data-ttu-id="57af2-200">A entrada deve existir no hive **do \_ \_ computador local hKey** .</span><span class="sxs-lookup"><span data-stu-id="57af2-200">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span>

<span data-ttu-id="57af2-201">Essa entrada fornece um servidor "Activate as Activator" com a mesma funcionalidade que o ROTFLAGS \_ ALLOWANYCLIENT fornece para um servidor runas.</span><span class="sxs-lookup"><span data-stu-id="57af2-201">This entry provides an "Activate As Activator" server with the same functionality that ROTFLAGS\_ALLOWANYCLIENT provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57af2-202">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57af2-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57af2-203">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="57af2-203">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="57af2-204">Compreendendo e trabalhando no Modo Protegido do Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="57af2-204">Understanding and Working in Protected Mode Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 