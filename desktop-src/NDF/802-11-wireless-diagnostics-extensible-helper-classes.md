---
title: 802,11 classes auxiliares extensíveis de diagnóstico sem fio
description: A infraestrutura interna de diagnóstico sem fio tem dois pontos de extensão. Auxiliar ClassPurposeRevised nativo Wi-Fi (RNWF) extensível auxiliar ClassDiagnoses problemas relacionados a extensões de conectividade 802,11.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104498992"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a><span data-ttu-id="10205-103">802,11 classes auxiliares extensíveis de diagnóstico sem fio</span><span class="sxs-lookup"><span data-stu-id="10205-103">802.11 Wireless Diagnostics Extensible Helper Classes</span></span>

<span data-ttu-id="10205-104">A infraestrutura interna de diagnóstico sem fio tem dois pontos de extensão.</span><span class="sxs-lookup"><span data-stu-id="10205-104">The built-in wireless diagnostics infrastructure has two extension points.</span></span>

| <span data-ttu-id="10205-105">Classe auxiliar pai</span><span class="sxs-lookup"><span data-stu-id="10205-105">Parent Helper Class</span></span>                                | <span data-ttu-id="10205-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="10205-106">Purpose</span></span>                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="10205-107">Classe auxiliar extensível RNWF (WiFi nativo) revisada</span><span class="sxs-lookup"><span data-stu-id="10205-107">Revised Native Wifi (RNWF) Extensible Helper Class</span></span> | <span data-ttu-id="10205-108">Diagnostica problemas relacionados a extensões de conectividade 802,11.</span><span class="sxs-lookup"><span data-stu-id="10205-108">Diagnoses issues related to 802.11 connectivity extensions.</span></span>       |
| <span data-ttu-id="10205-109">Classe auxiliar extensível L2Security</span><span class="sxs-lookup"><span data-stu-id="10205-109">L2Security Extensible Helper Class</span></span>                 | <span data-ttu-id="10205-110">Diagnostica problemas relacionados às extensões do protocolo de segurança de camada 2.</span><span class="sxs-lookup"><span data-stu-id="10205-110">Diagnoses issues related to Layer 2 security protocol extensions.</span></span> |



 

> [!Note]  
> <span data-ttu-id="10205-111">Uma classe auxiliar de terceiros deve se registrar com ambas as classes auxiliares pai para garantir que a classe de terceiros seja chamada.</span><span class="sxs-lookup"><span data-stu-id="10205-111">A third-party helper class should register with both parent helper classes to ensure that the third-party class gets called.</span></span> <span data-ttu-id="10205-112">Para obter mais informações sobre o registro, consulte [registrando extensões de classe auxiliar NDF](registering-ndf-helper-class-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="10205-112">For more information about registration, see [Registering NDF Helper Class Extensions](registering-ndf-helper-class-extensions.md).</span></span>

 

## <a name="rnwf-extensible-helper-class"></a><span data-ttu-id="10205-113">Classe auxiliar extensível RNWF</span><span class="sxs-lookup"><span data-stu-id="10205-113">RNWF Extensible Helper Class</span></span>

<span data-ttu-id="10205-114">Nome da classe auxiliar pai</span><span class="sxs-lookup"><span data-stu-id="10205-114">Parent Helper Class Name</span></span>

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

<span data-ttu-id="10205-115">A classe auxiliar extensível RNWF (WiFi nativo) revisada é o pai para classes auxiliares de terceiros que diagnosticam problemas relacionados à extensão de protocolos 802,11 usados por Wi-Fi nativo.</span><span class="sxs-lookup"><span data-stu-id="10205-115">The Revised Native Wifi (RNWF) extensible helper class is the parent for third-party helper classes that diagnose issues related to extending 802.11 protocols used by Native Wifi.</span></span>

<span data-ttu-id="10205-116">Os dois atributos de chave fornecidos pela classe auxiliar RNWF são o GUID da interface em que o problema ocorreu e o contexto de conexão.</span><span class="sxs-lookup"><span data-stu-id="10205-116">The two key attributes provided by the RNWF helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="10205-117">GUID da interface: esse atributo é denominado "ID da interface" e é do tipo **em \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="10205-117">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="10205-118">Contexto de conexão: esse atributo é denominado ID de rede e é do \_ tipo \_ cadeia de caracteres de octeto.</span><span class="sxs-lookup"><span data-stu-id="10205-118">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="10205-119">Essa cadeia de caracteres é, na verdade, um buffer da \_ estrutura de ID da WLAN WDIAG IHV \_ \_ definida em Wlanihv. h.</span><span class="sxs-lookup"><span data-stu-id="10205-119">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in Wlanihv.h.</span></span> <span data-ttu-id="10205-120">Essa estrutura é definida da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="10205-120">This structure is defined as follows.</span></span>

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> <span data-ttu-id="10205-121">**WDIAG \_ A \_ segurança do sinalizador de ID da WLAN do IHV \_ \_ \_ \_ habilitada** é o único valor de **dwFlags** possível.</span><span class="sxs-lookup"><span data-stu-id="10205-121">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="10205-122">O atributo correspondente para a classe auxiliar de terceiros deve ser igual à ID de serviço do seu módulo de software correspondente.</span><span class="sxs-lookup"><span data-stu-id="10205-122">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="10205-123">Esse também é o mesmo nome que a terceira parte deve ser registrada no registro.</span><span class="sxs-lookup"><span data-stu-id="10205-123">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="10205-124">O diagnóstico sem fio consultará a ID do serviço durante a sessão sem fio em que o problema ocorreu.</span><span class="sxs-lookup"><span data-stu-id="10205-124">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="10205-125">As informações serão retornadas para NDF, que determinará se a classe auxiliar de terceiros está presente e registrada e, em seguida, a chama.</span><span class="sxs-lookup"><span data-stu-id="10205-125">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="10205-126">A tabela a seguir lista os atributos correspondentes para a classe auxiliar extensível RNWF.</span><span class="sxs-lookup"><span data-stu-id="10205-126">The following table lists the matching attributes for the RNWF extensible helper class.</span></span>



| <span data-ttu-id="10205-127">Nome</span><span class="sxs-lookup"><span data-stu-id="10205-127">Name</span></span>          | <span data-ttu-id="10205-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="10205-128">Type</span></span>    | <span data-ttu-id="10205-129">Valor</span><span class="sxs-lookup"><span data-stu-id="10205-129">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="10205-130">Diagnosticsid</span><span class="sxs-lookup"><span data-stu-id="10205-130">DiagnosticsID</span></span> | <span data-ttu-id="10205-131">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="10205-131">REG\_SZ</span></span> | <span data-ttu-id="10205-132">\[Cadeia de \_ caracteres de GUID diagnosticsid \_</span><span class="sxs-lookup"><span data-stu-id="10205-132">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="l2security-extensible-helper-class"></a><span data-ttu-id="10205-133">Classe auxiliar extensível L2Security</span><span class="sxs-lookup"><span data-stu-id="10205-133">L2Security Extensible Helper Class</span></span>

<span data-ttu-id="10205-134">Nome da classe auxiliar pai</span><span class="sxs-lookup"><span data-stu-id="10205-134">Parent Helper Class Name</span></span>

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

<span data-ttu-id="10205-135">A classe auxiliar extensível de segurança de camada 2 (L2Security) é o pai para classes auxiliares de terceiros que diagnosticam problemas relacionados a serviços correspondentes e módulos de software que substituem a funcionalidade de segurança de camada 2.</span><span class="sxs-lookup"><span data-stu-id="10205-135">The Layer 2 Security (L2Security) extensible helper class is the parent for third-party helper classes that diagnose issues related to corresponding services and software modules that replace Layer 2 Security functionality.</span></span>

<span data-ttu-id="10205-136">Os dois atributos de chave fornecidos pela classe auxiliar de segurança de camada 2 são o GUID da interface em que o problema ocorreu e o contexto de conexão.</span><span class="sxs-lookup"><span data-stu-id="10205-136">The two key attributes provided by the Layer 2 Security helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="10205-137">GUID da interface: esse atributo é denominado "ID da interface" e é do tipo **em \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="10205-137">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="10205-138">Contexto de conexão: esse atributo é denominado ID de rede e é do \_ tipo \_ cadeia de caracteres de octeto.</span><span class="sxs-lookup"><span data-stu-id="10205-138">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="10205-139">Essa cadeia de caracteres é, na verdade, um buffer da \_ estrutura de ID da WLAN WDIAG IHV \_ \_ definida em wlanihv. h.</span><span class="sxs-lookup"><span data-stu-id="10205-139">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in wlanihv.h.</span></span> <span data-ttu-id="10205-140">Essa estrutura é definida da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="10205-140">This structure is defined as follows.</span></span>

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> <span data-ttu-id="10205-141">**WDIAG \_ A \_ segurança do sinalizador de ID da WLAN do IHV \_ \_ \_ \_ habilitada** é o único valor de **dwFlags** possível.</span><span class="sxs-lookup"><span data-stu-id="10205-141">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="10205-142">O atributo correspondente para a classe auxiliar de terceiros deve ser igual à ID de serviço do seu módulo de software correspondente.</span><span class="sxs-lookup"><span data-stu-id="10205-142">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="10205-143">Esse também é o mesmo nome que a terceira parte deve ser registrada no registro.</span><span class="sxs-lookup"><span data-stu-id="10205-143">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="10205-144">O diagnóstico sem fio consultará a ID do serviço durante a sessão sem fio em que o problema ocorreu.</span><span class="sxs-lookup"><span data-stu-id="10205-144">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="10205-145">As informações serão retornadas para NDF, que determinará se a classe auxiliar de terceiros está presente e registrada e, em seguida, a chama.</span><span class="sxs-lookup"><span data-stu-id="10205-145">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="10205-146">A tabela a seguir lista os atributos correspondentes para a classe auxiliar extensível de segurança de camada 2.</span><span class="sxs-lookup"><span data-stu-id="10205-146">The following table lists the matching attributes for the Layer 2 Security extensible helper class.</span></span>



| <span data-ttu-id="10205-147">Nome</span><span class="sxs-lookup"><span data-stu-id="10205-147">Name</span></span>          | <span data-ttu-id="10205-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="10205-148">Type</span></span>    | <span data-ttu-id="10205-149">Valor</span><span class="sxs-lookup"><span data-stu-id="10205-149">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="10205-150">Diagnosticsid</span><span class="sxs-lookup"><span data-stu-id="10205-150">DiagnosticsID</span></span> | <span data-ttu-id="10205-151">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="10205-151">REG\_SZ</span></span> | <span data-ttu-id="10205-152">\[Cadeia de \_ caracteres de GUID diagnosticsid \_</span><span class="sxs-lookup"><span data-stu-id="10205-152">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="matching-attributes"></a><span data-ttu-id="10205-153">Atributos correspondentes</span><span class="sxs-lookup"><span data-stu-id="10205-153">Matching Attributes</span></span>

<span data-ttu-id="10205-154">**Diagnosticsid**</span><span class="sxs-lookup"><span data-stu-id="10205-154">**DiagnosticsID**</span></span>

<span data-ttu-id="10205-155">802,11 o diagnóstico sem fio consultará o *diagnosticsid* do serviço de Wi-Fi nativo básico para descobrir se alguma extensão ou módulo de segurança de terceiros está instalado e envolvido na conexão.</span><span class="sxs-lookup"><span data-stu-id="10205-155">802.11 Wireless Diagnostics will query the *DiagnosticsID* from the core Native Wifi service in order to find out if any third-party wireless extensions or security modules are installed and involved in the connection.</span></span> <span data-ttu-id="10205-156">O diagnóstico sem fio, em seguida, fornecerá as subclasses a essas classes auxiliares de terceiros usando o *diagnosticsid* como o atributo correspondente.</span><span class="sxs-lookup"><span data-stu-id="10205-156">Wireless Diagnostics will then provide hypotheses to these third-party helper classes using the *DiagnosticsID* as the matching attribute.</span></span> <span data-ttu-id="10205-157">Todas as classes auxiliares de terceiros devem ser incluídas no e instaladas com o pacote de driver associado.</span><span class="sxs-lookup"><span data-stu-id="10205-157">Any third-party helper classes should be included in and installed with the associated driver package.</span></span> <span data-ttu-id="10205-158">O *diagnosticsid* será definido no arquivo INF da miniporta como uma chave do registro na diretiva [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) .</span><span class="sxs-lookup"><span data-stu-id="10205-158">The *DiagnosticsID* will be defined in the miniport INF file as a registry key in the [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) directive.</span></span>

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

<span data-ttu-id="10205-159">Essa chave define a ID da classe auxiliar sem fio para o módulo de software de terceiros.</span><span class="sxs-lookup"><span data-stu-id="10205-159">This key defines the ID of the wireless helper class for the third-party software module.</span></span> <span data-ttu-id="10205-160">Essa chave é opcional para a estrutura de extensibilidade, mas é necessária se a implementação inclui uma classe auxiliar sem fio do IHV que se conecta ao NDF e pode diagnosticar problemas de conectividade relacionados às extensões sem fio ou de segurança do RNWF.</span><span class="sxs-lookup"><span data-stu-id="10205-160">This key is optional for the extensibility framework, but it is needed if the implementation includes an IHV Wireless Helper Class that plugs into NDF and can diagnose connectivity problems related to the RNWF wireless or security extensions.</span></span> <span data-ttu-id="10205-161">As classes auxiliares de diagnóstico de WLAN da MS consultarão essa ID do serviço de configuração automática sem fio quando os módulos IHV forem instalados e fornecerão essa ID como a referência ou o atributo correspondente ao NDF durante uma sessão de diagnóstico para que o NDF possa chamar a classe auxiliar sem fio de terceiros apropriada quando necessário.</span><span class="sxs-lookup"><span data-stu-id="10205-161">MS WLAN diagnostics helper classes will query this ID from the Wireless Auto Configuration Service when IHV modules are installed and will provide this ID as the reference or matching attribute to NDF during a diagnostics session so that NDF can call the appropriate third-party wireless helper class when necessary.</span></span>

<span data-ttu-id="10205-162">**\[Cadeia de \_ caracteres de GUID diagnosticsid \_\]**</span><span class="sxs-lookup"><span data-stu-id="10205-162">**\[DiagnosticsID\_GUID\_String\]**</span></span>

<span data-ttu-id="10205-163">Esse valor deve ser uma cadeia de caracteres com todas as letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="10205-163">This value must be a string of all uppercase letters.</span></span> <span data-ttu-id="10205-164">Por exemplo, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span><span class="sxs-lookup"><span data-stu-id="10205-164">For example, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span></span>

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a><span data-ttu-id="10205-165">Escopo de classes auxiliares de diagnóstico sem fio 802,11</span><span class="sxs-lookup"><span data-stu-id="10205-165">Scope of 802.11 Wireless Diagnostics Helper Classes</span></span>

<span data-ttu-id="10205-166">802,11 classes auxiliares de diagnóstico sem fio atualmente diagnosticam problemas sem fio nas áreas a seguir.</span><span class="sxs-lookup"><span data-stu-id="10205-166">802.11 wireless diagnostics helper classes currently diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="10205-167">Quaisquer problemas de conectividade de 802,11, incluindo a associação de 802,11, a autenticação 802,11, as configurações de segurança 802,11 relacionadas aos padrões do 802,11 & protocolos com suporte nativo no sistema operacional e problemas de desempenho.</span><span class="sxs-lookup"><span data-stu-id="10205-167">Any 802.11 connectivity issues including 802.11 association, 802.11 authentication, 802.11 security settings related to 802.11 standards & protocols natively supported in the operating system, and performance issues.</span></span>
-   <span data-ttu-id="10205-168">Problemas de segurança de camada 2 com relação às configurações de 802.1 x e quaisquer problemas relacionados à autenticação de camada 2 usando métodos com suporte nativo no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="10205-168">Layer 2 Security issues with regards to 802.1x configurations and any issues related to layer 2 authentication using methods natively supported on Windows Vista and Windows Server 2008.</span></span>
-   <span data-ttu-id="10205-169">Incompatibilidades de configuração nas configurações de perfil entre o cliente e o ponto de acesso ou a infraestrutura de rede e serviços.</span><span class="sxs-lookup"><span data-stu-id="10205-169">Configuration mismatches in profile settings between the client and the Access Point or the network infrastructure and services.</span></span>

<span data-ttu-id="10205-170">as classes auxiliares de diagnóstico sem fio 802,11 atualmente não diagnosticam problemas sem fio nas áreas a seguir.</span><span class="sxs-lookup"><span data-stu-id="10205-170">802.11 wireless diagnostics helper classes currently do not diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="10205-171">Problemas relacionados a extensões 802,11 de terceiros, incluindo quaisquer configurações de perfil ou driver relacionadas a essas extensões.</span><span class="sxs-lookup"><span data-stu-id="10205-171">Issues related to third-party 802.11 extensions including any profile or driver settings related to these extensions.</span></span>
-   <span data-ttu-id="10205-172">Problemas relacionados a métodos EAP de terceiros.</span><span class="sxs-lookup"><span data-stu-id="10205-172">Issues related to third-party EAP methods.</span></span>
-   <span data-ttu-id="10205-173">Problemas do driver de miniporta sem fio.</span><span class="sxs-lookup"><span data-stu-id="10205-173">Wireless miniport driver issues.</span></span>
-   <span data-ttu-id="10205-174">Qualquer protocolo de segurança 802,11 e camada 2 ou problemas relacionados a padrões que não têm suporte nativo.</span><span class="sxs-lookup"><span data-stu-id="10205-174">Any 802.11 and layer 2 security protocol or standards-related issues that are not natively supported.</span></span>
-   <span data-ttu-id="10205-175">Problemas no nível do sistema ou do componente que podem afetar a conectividade sem fio, como gerenciamento de energia, pouco espaço em disco, condições de memória e problemas de hardware.</span><span class="sxs-lookup"><span data-stu-id="10205-175">System or component-level issues that might impact wireless connectivity, such as power management, low disk space, memory conditions, and hardware problems.</span></span>

<span data-ttu-id="10205-176">Além disso, 802,11 o diagnóstico sem fio não analisa casos [**highutilization dos**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) .</span><span class="sxs-lookup"><span data-stu-id="10205-176">Additionally, 802.11 Wireless Diagnostics does not analyze [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) cases.</span></span> <span data-ttu-id="10205-177">Os problemas de desempenho sem fio identificados serão analisados e relatados como casos [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .</span><span class="sxs-lookup"><span data-stu-id="10205-177">Identified wireless performance issues will be analyzed and reported as [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) cases.</span></span>

 

 




