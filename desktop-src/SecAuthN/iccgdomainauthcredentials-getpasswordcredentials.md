---
description: Retorna credenciais para autenticar um contêiner não ingressado no domínio com Active Directory.
title: 'Método ICcgDomainAuthCredentials:: GetPasswordCredentials (ccgplugins. h)'
ms.topic: reference
ms.date: 10/21/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials.GetPasswordCredentials
api_type:
- COM
api_location:
- ccgplugins.h
ms.openlocfilehash: abd70a109e491773b374ae32787760d265167baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794637"
---
# <a name="iccgdomainauthcredentialsgetpasswordcredentials-method"></a><span data-ttu-id="4e6b3-103">Método ICcgDomainAuthCredentials:: GetPasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="4e6b3-103">ICcgDomainAuthCredentials::GetPasswordCredentials method</span></span>

<span data-ttu-id="4e6b3-104">Retorna credenciais para autenticar um contêiner não ingressado no domínio com Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-104">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e6b3-105">Syntax</span></span>


```C++
HRESULT GetPasswordCredentials(
[in] LPCWSTR pluginInput, 
[out] LPWSTR* domainName, 
[out] LPWSTR* username, 
[out] LPWSTR* password);
);
```



## <a name="parameters"></a><span data-ttu-id="4e6b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e6b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e6b3-107">*pluginInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e6b3-107">*pluginInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6b3-108">Uma cadeia de caracteres de entrada passada pelo tempo de execução do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-108">An input string passed in by the container runtime.</span></span> <span data-ttu-id="4e6b3-109">A implementação do cliente usa a cadeia de caracteres de entrada fornecida para recuperar as credenciais de autenticação, normalmente de um provedor de armazenamento seguro, que são retornadas nos parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-109">The client implementation uses the provided input string to retrieve authentication credentials, typically from a secure storage provider, that are returned in the output parameters.</span></span> <span data-ttu-id="4e6b3-110">A cadeia de caracteres de entrada é fornecida para os serviços de computação do host (HCS) em um arquivo de especificação de credencial.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-110">The input string is provided to the Host Compute Services (HCS) in a credential specification file.</span></span> <span data-ttu-id="4e6b3-111">Para obter mais informações, consulte a seção **comentários** .</span><span class="sxs-lookup"><span data-stu-id="4e6b3-111">For more information, see the **Remarks** section.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4e6b3-112">*nome_do_domínio* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4e6b3-112">*domainName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6b3-113">O nome de domínio para as credenciais.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-113">The domain name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4e6b3-114">*nome de usuário* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4e6b3-114">*username* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6b3-115">O nome de usuário para as credenciais.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-115">The user name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4e6b3-116">*senha* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4e6b3-116">*password* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e6b3-117">A senha para as credenciais.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-117">The password for the credentials.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e6b3-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e6b3-118">Return value</span></span>

<span data-ttu-id="4e6b3-119">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-119">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4e6b3-120">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-120">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e6b3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e6b3-121">Remarks</span></span>

<span data-ttu-id="4e6b3-122">A API pode ser chamada simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-122">The API may be called concurrently.</span></span> <span data-ttu-id="4e6b3-123">Portanto, o desenvolvedor precisa garantir que sua implementação seja thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-123">Therefore, the developer needs to ensure that their implementation is thread safe.</span></span> <span data-ttu-id="4e6b3-124">Além disso, o objeto COM será ativado fora do processo e deverá ser registrado adequadamente.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-124">Additionally, the COM object will be activated out-of-proc and it must be registered appropriately.</span></span> 

<span data-ttu-id="4e6b3-125">O implementador deve adicionar uma chave em "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses" para seu CLSID COM.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-125">The implementer must add a key under “HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses” for their COM CLSID.</span></span> <span data-ttu-id="4e6b3-126">O acesso de gravação a "CCG\COMClasses" é restrito a contas de sistema e administrador.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-126">Write access to “CCG\COMClasses” is restricted to SYSTEM and Administrator accounts.</span></span> 

<span data-ttu-id="4e6b3-127">A seguir está um exemplo de arquivo de especificação de credencial.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-127">The following is an example credential specification file.</span></span> <span data-ttu-id="4e6b3-128">Para obter informações sobre como fornecer esse arquivo para o Docker, consulte [executar um contêiner com um gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span><span class="sxs-lookup"><span data-stu-id="4e6b3-128">For information on supplying this file to Docker, see [Run a container with a gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span></span>

```json
{
    "CmsPlugins": [
        "ActiveDirectory"
    ],
    "DomainJoinConfig": {
        "Sid": "S-1-5-21-3700119848-2853083131-2094573802",
        "MachineAccountName": "gmsa1",
        "Guid": "630a7dd3-2d3e-4471-ae91-1d9ea2556cd5",
        "DnsTreeName": "contoso.com",
        "DnsName": "contoso.com",
        "NetBiosName": "CONTOSO"
    },
    "ActiveDirectoryConfig": {
        "GroupManagedServiceAccounts": [
            {
                "Name": "gmsa1",
                "Scope": "contoso.com"
            },
            {
                "Name": "gmsa1",
                "Scope": "CONTOSO"
            }
        ],
        "HostAccountConfig": {
            "PortableCcgVersion": "1",
            "PluginGUID": "{CFCA0441-511D-4B2A-862E-20348A78760B}",
            "PluginInput": "contoso.com:gmsaccg:<password>"
        }
    }
}

```

## <a name="examples"></a><span data-ttu-id="4e6b3-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e6b3-129">Examples</span></span>

<span data-ttu-id="4e6b3-130">O exemplo a seguir mostra uma implementação simples de **ICcgDomainAuthCredentials**.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-130">The following example shows a simple implementation of **ICcgDomainAuthCredentials**.</span></span> <span data-ttu-id="4e6b3-131">Observe que, para fins ilustrativos, este exemplo obtém as credenciais simplesmente analisando a cadeia de caracteres de entrada.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-131">Note that, for illustrative purposes, this sample obtains the credentials by simply parsing the input string.</span></span> <span data-ttu-id="4e6b3-132">Uma implementação do mundo real armazenará as credenciais em um repositório de dados seguro e usará a cadeia de caracteres de entrada para localizar as informações de credenciais.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-132">A real-world implementation would store the credentials in a secure data store and use the input string to locate the credential information.</span></span> <span data-ttu-id="4e6b3-133">Além disso, as implementações do método COM padrão foram omitidas desta amostra para fins de brevidade.</span><span class="sxs-lookup"><span data-stu-id="4e6b3-133">Also, the standard COM method implementations have been omitted from this sample for brevity.</span></span>


```C++
// UUID generated by the developer
[uuid("cfca0441-511d-4b2a-862e-20348a78760b")] 
class CCGStubPlugin : public RuntimeClass<RuntimeClassFlags<RuntimeClassType::ClassicCom>, ICcgDomainAuthCredentials >
{
   public:
    CCGStubPlugin() {}

    ~CCGStubPlugin() {}

    IFACEMETHODIMP GetPasswordCredentials(
        _In_ LPCWSTR pluginInput,
        _Outptr_ LPWSTR *domainName,
        _Outptr_ LPWSTR *username,
        _Outptr_ LPWSTR *password)
    {
        std::wstring domainParsed, userParsed, passwordParsed; 
        try
        {
            if(domainName == NULL || username == NULL || password == NULL)
            {
                return STG_E_INVALIDPARAMETER;
            }
            *domainName = NULL;
            *username = NULL;
            *password = NULL;
            wstring pluginInputString(pluginInput);
            if (count(pluginInputString.begin(), pluginInputString.end(), ':') < 2)
            {
                return CO_E_NOT_SUPPORTED;
            }
            // Extract creds of this format Domain:Username:Password
            size_t sep1 = pluginInputString.find(L":");
            size_t sep2 = pluginInputString.find(L":", sep1 + 1);
            domainParsed = pluginInputString.substr(0, sep1);
            userParsed = pluginInputString.substr(sep1 + 1, sep2 - sep1 - 1);
            passwordParsed = pluginInputString.substr(sep2 + 1);
        }
        catch (...)
        {
            return EVENT_E_INTERNALERROR;
        }

        auto userCo = wil::make_cotaskmem_string_nothrow(userParsed.c_str());
        auto passwordCo = wil::make_cotaskmem_string_nothrow(passwordParsed.c_str());
        auto domainCo = wil::make_cotaskmem_string_nothrow(domainParsed.c_str());
        if (userCo == nullptr || passwordCo == nullptr || domainCo == nullptr)
        {
            return STG_E_INSUFFICIENTMEMORY;
        }

        *domainName = domainCo.release();
        *username = userCo.release();
        *password = passwordCo.release();
        return S_OK;
    }
};
CoCreatableClass(CCGStubPlugin);

```



## <a name="requirements"></a><span data-ttu-id="4e6b3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e6b3-134">Requirements</span></span>




| <span data-ttu-id="4e6b3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e6b3-135">Requirement</span></span> | <span data-ttu-id="4e6b3-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4e6b3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6b3-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e6b3-137">Minimum supported server</span></span> | <span data-ttu-id="4e6b3-138">Windows Server, versão 2004</span><span class="sxs-lookup"><span data-stu-id="4e6b3-138">Windows Server, version 2004</span></span>                                    |
| <span data-ttu-id="4e6b3-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e6b3-139">Header</span></span>                   | <span data-ttu-id="4e6b3-140">ccgplugins. h</span><span class="sxs-lookup"><span data-stu-id="4e6b3-140">ccgplugins.h</span></span>   |
| <span data-ttu-id="4e6b3-141">IID</span><span class="sxs-lookup"><span data-stu-id="4e6b3-141">IID</span></span>                    | <span data-ttu-id="4e6b3-142">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="4e6b3-142">6ecda518-2010-4437-8bc3-46e752b7b172</span></span>          |



 

