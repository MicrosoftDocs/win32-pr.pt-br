---
description: API do codificador
ms.assetid: 3d19152f-17a3-4576-a2a2-5b827d9ca8d1
title: API do codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 386b964f44dc4dc69896ead34bbe0d0177b198a1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370277"
---
# <a name="encoder-api"></a><span data-ttu-id="85e3a-103">API do codificador</span><span class="sxs-lookup"><span data-stu-id="85e3a-103">Encoder API</span></span>

<span data-ttu-id="85e3a-104">A API do codificador fornece uma interface uniforme para configurar o software e os codificadores de hardware.</span><span class="sxs-lookup"><span data-stu-id="85e3a-104">The Encoder API provides a uniform interface for configuring software and hardware encoders.</span></span> <span data-ttu-id="85e3a-105">Os aplicativos podem usar a API do codificador para configurar um codificador e armazenar as definições de configuração.</span><span class="sxs-lookup"><span data-stu-id="85e3a-105">Applications can use the Encoder API to configure an encoder and to store the configuration settings.</span></span> <span data-ttu-id="85e3a-106">Os fornecedores de codificador podem usar a API do codificador para expor os recursos de um codificador.</span><span class="sxs-lookup"><span data-stu-id="85e3a-106">Encoder vendors can use the Encoder API to expose the capabilities of an encoder.</span></span> <span data-ttu-id="85e3a-107">Embora a API do codificador seja projetada principalmente para codificadores, é geral o suficiente para que os decodificadores também possam dar suporte a ela.</span><span class="sxs-lookup"><span data-stu-id="85e3a-107">Although the Encoder API is designed primarily for encoders, it is general enough that decoders can support it as well.</span></span>

<span data-ttu-id="85e3a-108">A API do codificador é exposta aos aplicativos por meio da interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) , que é exposta pelo filtro do codificador.</span><span class="sxs-lookup"><span data-stu-id="85e3a-108">The Encoder API is exposed to applications through the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface, which is exposed by the encoder filter.</span></span> <span data-ttu-id="85e3a-109">O filtro do codificador pode ser um filtro do DirectShow nativo, um codificador de hardware ou um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="85e3a-109">The encoder filter may be a native DirectShow filter, a hardware encoder, or a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="85e3a-110">Filtros de software: um codificador que é implementado como um filtro do DirectShow nativo deve expor o [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) diretamente.</span><span class="sxs-lookup"><span data-stu-id="85e3a-110">Software filters: An encoder that is implemented as a native DirectShow filter should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) directly.</span></span>
-   <span data-ttu-id="85e3a-111">Codificadores de hardware: o dispositivo de codificação é exposto por meio de um ou mais AVStream minidrivers, que são representados no modo de usuário pelo KSProxy.</span><span class="sxs-lookup"><span data-stu-id="85e3a-111">Hardware encoders: The encoding device is exposed through one or more AVStream minidrivers, which are represented in user mode by KSProxy.</span></span> <span data-ttu-id="85e3a-112">KSProxy converte chamadas de método [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) em conjuntos de propriedades KS.</span><span class="sxs-lookup"><span data-stu-id="85e3a-112">KSProxy translates [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) method calls into KS property sets.</span></span> <span data-ttu-id="85e3a-113">Para obter mais informações, consulte a documentação do DDK.</span><span class="sxs-lookup"><span data-stu-id="85e3a-113">For more information, see the DDK documentation.</span></span>
-   <span data-ttu-id="85e3a-114">DMOs: o DMO deve expor a interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="85e3a-114">DMOs: The DMO should expose the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="85e3a-115">Os aplicativos do DirectShow podem consultar o filtro de invólucro do DMO, que expõe a interface agregando o DMO.</span><span class="sxs-lookup"><span data-stu-id="85e3a-115">DirectShow applications can query the DMO Wrapper filter, which exposes the interface by aggregating the DMO.</span></span> <span data-ttu-id="85e3a-116">Aplicativos não baseados no DirectShow podem consultar o DMO diretamente.</span><span class="sxs-lookup"><span data-stu-id="85e3a-116">Applications not based on DirectShow can query the DMO directly.</span></span>

### <a name="encoder-capabilties"></a><span data-ttu-id="85e3a-117">Funcionalidades do codificador</span><span class="sxs-lookup"><span data-stu-id="85e3a-117">Encoder Capabilties</span></span>

<span data-ttu-id="85e3a-118">Um codificador pode registrar uma lista de recursos de alto nível armazenando-os no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="85e3a-118">An encoder can register a list of high-level capabilities by storing them in the system registry.</span></span> <span data-ttu-id="85e3a-119">Cada recurso é identificado por um GUID.</span><span class="sxs-lookup"><span data-stu-id="85e3a-119">Each capability is identified by a GUID.</span></span> <span data-ttu-id="85e3a-120">Para enumerar os recursos de um codificador específico, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="85e3a-120">To enumerate the capabilities of a particular encoder, do the following:</span></span>

1.  <span data-ttu-id="85e3a-121">Crie o moniker que representa o filtro do codificador.</span><span class="sxs-lookup"><span data-stu-id="85e3a-121">Create the moniker that represents the encoder filter.</span></span> <span data-ttu-id="85e3a-122">(Consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).)</span><span class="sxs-lookup"><span data-stu-id="85e3a-122">(See [Using the System Device Enumerator](using-the-system-device-enumerator.md).)</span></span>
2.  <span data-ttu-id="85e3a-123">Consulte o moniker do filtro para a interface [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) .</span><span class="sxs-lookup"><span data-stu-id="85e3a-123">Query the filter moniker for the [**IGetCapabilitiesKey**](/windows/desktop/api/Strmif/nn-strmif-igetcapabilitieskey) interface.</span></span>
3.  <span data-ttu-id="85e3a-124">Chame [**IGetCapabilitiesKey:: GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span><span class="sxs-lookup"><span data-stu-id="85e3a-124">Call [**IGetCapabilitiesKey::GetCapabilitiesKey**](/windows/desktop/api/Strmif/nf-strmif-igetcapabilitieskey-getcapabilitieskey).</span></span> <span data-ttu-id="85e3a-125">O método retorna um identificador para a chave do registro que contém a lista de recursos do filtro.</span><span class="sxs-lookup"><span data-stu-id="85e3a-125">The method returns a handle to the registry key that contains the filter's capabilities list.</span></span>
4.  <span data-ttu-id="85e3a-126">Chame a função **RegEnumValue** para enumerar os valores para a chave retornada.</span><span class="sxs-lookup"><span data-stu-id="85e3a-126">Call the **RegEnumValue** function to enumerate the values for the returned key.</span></span>

<span data-ttu-id="85e3a-127">Se você estiver desenvolverndo um codificador, crie as entradas do registro para os recursos quando o filtro for registrado.</span><span class="sxs-lookup"><span data-stu-id="85e3a-127">If you are devloping an encoder, create the registry entries for the capabilities when the filter is registered.</span></span> <span data-ttu-id="85e3a-128">Para filtros de software, crie uma chave chamada **recursos** que seja adjacente às chaves **FilterData** e **FriendlyName** .</span><span class="sxs-lookup"><span data-stu-id="85e3a-128">For software filters, create a key named **Capabilities** that is adjacent to the **FilterData** and **FriendlyName** keys.</span></span> <span data-ttu-id="85e3a-129">Normalmente, você adicionaria essas informações depois de chamar [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) para registrar os dados de filtro padrão.</span><span class="sxs-lookup"><span data-stu-id="85e3a-129">Typically, you would add this information after calling [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) to register the standard filter data.</span></span> <span data-ttu-id="85e3a-130">Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="85e3a-130">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span> <span data-ttu-id="85e3a-131">Como alternativa, você pode criar uma chave **CapabilitiesLocation** que contém uma cadeia de caracteres fornecendo a localização da chave de **recursos** no registro.</span><span class="sxs-lookup"><span data-stu-id="85e3a-131">Alternatively, you can create a **CapabilitiesLocation** key that contains a string giving the location of the **Capabilities** key in the registry.</span></span> <span data-ttu-id="85e3a-132">A cadeia de caracteres deve começar com "HKLM \\ ", "HKCR \\ " ou "HKCU \\ " para indicar a subárvore do registro.</span><span class="sxs-lookup"><span data-stu-id="85e3a-132">The string should start with "HKLM\\", "HKCR\\", or "HKCU\\" to indicate the registry subtree.</span></span> <span data-ttu-id="85e3a-133">Para dispositivos Plug and Play, os arquivos de instalação do driver devem criar uma chave de **recursos** adjacente à chave **FriendlyName** do filtro ou usar uma chave **CapabilitiesLocation** , conforme descrito em filtros de software.</span><span class="sxs-lookup"><span data-stu-id="85e3a-133">For Plug and Play devices, the driver's setup files should create a **Capabilities** key adjacent to the filter's **FriendlyName** key, or it can use a **CapabilitiesLocation** key as described for software filters.</span></span>

<span data-ttu-id="85e3a-134">Depois de criar a chave de **recursos** , crie um valor para cada GUID de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="85e3a-134">Once you have created the **Capabilities** key, create a value for each capability GUID.</span></span> <span data-ttu-id="85e3a-135">O nome do valor deve ser a forma de cadeia de caracteres do GUID, no formato `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}` .</span><span class="sxs-lookup"><span data-stu-id="85e3a-135">The name of the value should be the string form of the GUID, in the form `{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}`.</span></span> <span data-ttu-id="85e3a-136">Cada tipo de valor deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="85e3a-136">Each value type should be one of the following:</span></span>

-   <span data-ttu-id="85e3a-137">Valor numérico único.</span><span class="sxs-lookup"><span data-stu-id="85e3a-137">Single numerical value.</span></span> <span data-ttu-id="85e3a-138">Use um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="85e3a-138">Use a **DWORD** value.</span></span>
-   <span data-ttu-id="85e3a-139">GUID.</span><span class="sxs-lookup"><span data-stu-id="85e3a-139">GUID.</span></span> <span data-ttu-id="85e3a-140">Use a forma de cadeia de caracteres do GUID.</span><span class="sxs-lookup"><span data-stu-id="85e3a-140">Use the string form of the GUID.</span></span>
-   <span data-ttu-id="85e3a-141">Pares numéricos.</span><span class="sxs-lookup"><span data-stu-id="85e3a-141">Numeric pairs.</span></span> <span data-ttu-id="85e3a-142">Use uma cadeia de caracteres com o formato "a, b" para representar pares de valores, como largura e altura, ou numerador e denominador para frações.</span><span class="sxs-lookup"><span data-stu-id="85e3a-142">Use a string with the form "a,b" to represent pairs of values, such as width and height, or numerator and denominator for fractions.</span></span>
-   <span data-ttu-id="85e3a-143">Matrizes de valores.</span><span class="sxs-lookup"><span data-stu-id="85e3a-143">Arrays of values.</span></span> <span data-ttu-id="85e3a-144">Use várias cadeias de caracteres (**reg \_ sz \_ multi**) para representar mais de um valor.</span><span class="sxs-lookup"><span data-stu-id="85e3a-144">Use multi-strings (**REG\_SZ\_MULTI**) to represent more than one value.</span></span>

<span data-ttu-id="85e3a-145">O exemplo a seguir mostra o layout do registro para um filtro de software:</span><span class="sxs-lookup"><span data-stu-id="85e3a-145">The following example shows the registry layout for a software filter:</span></span>


```C++
\HKCR\CLSID\Filter Category\Instance\Filter CLSID\Capabilities\
    
Values: 
    
    guid1: 1234 (REG_DWORD)   
    
    guid2: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}" (REG_SZ)
    
    guid3: "2","4","6" (REG_SZ_MULTI)
    
    guid4: "720,480" (REG_SZ) 
```



### <a name="encoder-profiles"></a><span data-ttu-id="85e3a-146">Perfis de codificador</span><span class="sxs-lookup"><span data-stu-id="85e3a-146">Encoder Profiles</span></span>

<span data-ttu-id="85e3a-147">Um *perfil de codificador* é uma lista fixa de definições de configuração que podem ser aplicadas a um codificador em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="85e3a-147">An *encoder profile* is a fixed list of configuration settings that can be applied to an encoder at run time.</span></span> <span data-ttu-id="85e3a-148">Os perfis são independentes do codificador; um aplicativo pode selecionar um codificador e, em seguida, selecionar um perfil e aplicar as configurações de perfil ao codificador.</span><span class="sxs-lookup"><span data-stu-id="85e3a-148">Profiles are independent of the encoder; an application can select an encoder, then select a profile and apply the profile settings to the encoder.</span></span> <span data-ttu-id="85e3a-149">Os perfis são identificados por GUID e devem ser armazenados no seguinte local no registro:</span><span class="sxs-lookup"><span data-stu-id="85e3a-149">Profiles are identified by GUID and should be stored in the following location in the registry:</span></span>


```C++
\HKLM\Software\Microsoft\EncoderProfiles\Profile GUID\
```



<span data-ttu-id="85e3a-150">em que *GUID do perfil*</span><span class="sxs-lookup"><span data-stu-id="85e3a-150">where *Profile GUID*</span></span>

<span data-ttu-id="85e3a-151">é a forma de cadeia de caracteres do GUID que identifica o perfil.</span><span class="sxs-lookup"><span data-stu-id="85e3a-151">is the string form of the GUID that identifies the profile.</span></span> <span data-ttu-id="85e3a-152">Crie valores para cada configuração.</span><span class="sxs-lookup"><span data-stu-id="85e3a-152">Create values for each setting.</span></span> <span data-ttu-id="85e3a-153">Além disso, crie um valor de cadeia de caracteres chamado "FriendlyName" cujos dados identificam o perfil (como "LowBandwidthVideo").</span><span class="sxs-lookup"><span data-stu-id="85e3a-153">Also create a string value named "FriendlyName" whose data identifies the profile (such as "LowBandwidthVideo").</span></span>

## <a name="related-topics"></a><span data-ttu-id="85e3a-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85e3a-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85e3a-155">Codificador e desenvolvimento de decodificador</span><span class="sxs-lookup"><span data-stu-id="85e3a-155">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



