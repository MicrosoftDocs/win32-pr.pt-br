---
description: Requisitos para aplicativos do Windows Media DRM-Enabled
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Requisitos para aplicativos do Windows Media DRM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105764238"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a><span data-ttu-id="bd450-103">Requisitos para aplicativos do Windows Media DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="bd450-103">Requirements for Windows Media DRM-Enabled Applications</span></span>

<span data-ttu-id="bd450-104">Para criar um aplicativo habilitado para Windows Media Digital Rights Management (DRM), você deve ter os cabeçalhos e as bibliotecas descritos na seção [requisitos gerais para o desenvolvimento de aplicativos](general-requirements-for-application-development.md) deste documento.</span><span class="sxs-lookup"><span data-stu-id="bd450-104">To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document.</span></span> <span data-ttu-id="bd450-105">Além disso, o aplicativo precisará fornecer propriedades adicionais nas informações do cliente ao abrir o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd450-105">In addition, the application will need to supply additional properties in the client information when opening the device.</span></span>

<span data-ttu-id="bd450-106">As duas propriedades adicionais que são necessárias para habilitar transferências de conteúdo protegidas por DRM do Windows Media são descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd450-106">The two additional properties that are required to enable Windows Media DRM-protected content transfers are described in the following table.</span></span>



| <span data-ttu-id="bd450-107">Propriedade</span><span class="sxs-lookup"><span data-stu-id="bd450-107">Property</span></span>                                      | <span data-ttu-id="bd450-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd450-108">Description</span></span>                              |
|-----------------------------------------------|------------------------------------------|
| <span data-ttu-id="bd450-109">\_ \_ \_ chave privada do aplicativo \_ de cliente WPD \_</span><span class="sxs-lookup"><span data-stu-id="bd450-109">WPD\_CLIENT\_WMDRM\_APPLICATION\_PRIVATE\_KEY</span></span> | <span data-ttu-id="bd450-110">Especifica a chave privada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd450-110">Specifies the application's private key.</span></span> |
| <span data-ttu-id="bd450-111">\_certificado de \_ aplicativo de WMDRM cliente \_ WPD \_</span><span class="sxs-lookup"><span data-stu-id="bd450-111">WPD\_CLIENT\_WMDRM\_APPLICATION\_CERTIFICATE</span></span>  | <span data-ttu-id="bd450-112">Especifica o certificado do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd450-112">Specifies the application's certificate.</span></span> |



 

<span data-ttu-id="bd450-113">Essas propriedades devem ser fornecidas nas informações do cliente do aplicativo quando o dispositivo for aberto com o método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .</span><span class="sxs-lookup"><span data-stu-id="bd450-113">These properties must be supplied in the application's client information when the device is opened with the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.</span></span> <span data-ttu-id="bd450-114">Quando essas propriedades são fornecidas, a API WPD permite transferências de conteúdo protegidas.</span><span class="sxs-lookup"><span data-stu-id="bd450-114">When these properties are supplied, the WPD API allows protected content transfers.</span></span> <span data-ttu-id="bd450-115">Se o aplicativo tiver fornecido um certificado e uma chave privada, a API criará um canal seguro para transferir conteúdo WMDRM protegido para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bd450-115">If the application has provided a certificate and private key, the API will create a secure channel to transfer protected WMDRM content to the device.</span></span>

<span data-ttu-id="bd450-116">Para obter informações sobre como criar e distribuir aplicativos baseados no Windows que dão suporte ao Windows Media DRM, consulte o tópico [Licenciamento de aplicativos baseados no Windows](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd450-116">For information about creating and distributing Windows-based applications that support Windows Media DRM, see the following [Licensing Windows-based Applications](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) topic.</span></span>

## <a name="transferring-content"></a><span data-ttu-id="bd450-117">Transferindo conteúdo</span><span class="sxs-lookup"><span data-stu-id="bd450-117">Transferring Content</span></span>

<span data-ttu-id="bd450-118">Para transferir conteúdo protegido por WMDRM, use [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="bd450-118">To transfer WMDRM protected content, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="bd450-119">Esse método pode ser usado para conteúdo protegido e não criptografado sem opções adicionais.</span><span class="sxs-lookup"><span data-stu-id="bd450-119">This method can be used for both protected and clear content without additional options.</span></span> <span data-ttu-id="bd450-120">A API WPD selecionará automaticamente o canal protegido ou não criptografado, dependendo se o conteúdo está protegido ou claro.</span><span class="sxs-lookup"><span data-stu-id="bd450-120">The WPD API will automatically select the protected or clear channel depending on whether the content is protected or clear.</span></span> <span data-ttu-id="bd450-121">Ele interage com o provedor de conteúdo do WMDRM Secure para processar as licenças WMDRM.</span><span class="sxs-lookup"><span data-stu-id="bd450-121">It interfaces with the WMDRM Secure Content Provider to process the WMDRM licenses.</span></span>

## <a name="transferring-known-clear-content"></a><span data-ttu-id="bd450-122">Transferindo conteúdo de limpeza conhecido</span><span class="sxs-lookup"><span data-stu-id="bd450-122">Transferring Known Clear Content</span></span>

<span data-ttu-id="bd450-123">Se você habilitou seu aplicativo para lidar com o conteúdo protegido, mas souber que um arquivo específico não está protegido, você pode informar a WPD para ignorar o processamento de DRM ao definir a opção de **API WPD use a opção de \_ \_ \_ \_ \_ \_ fluxo de dados CLEAR** como true no **IPortableDeviceValues** de entrada ao chamar [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para limpar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bd450-123">If you've enabled your application to handle protected content, but you know that a specific file is not protected, you can tell WPD to skip the DRM processing by setting **WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM** option to TRUE in the input **IPortableDeviceValues** when calling [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) for clear content.</span></span>

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a><span data-ttu-id="bd450-124">Acessando operações de medição usando IWMDRMDeviceApp</span><span class="sxs-lookup"><span data-stu-id="bd450-124">Accessing Metering Operations using IWMDRMDeviceApp</span></span>

<span data-ttu-id="bd450-125">O WPD fornece um mecanismo para acessar as APIs do **IWMDRMDeviceApp** para atualizações de licenças e a recuperação de dados de medição.</span><span class="sxs-lookup"><span data-stu-id="bd450-125">WPD provides a mechanism to access the **IWMDRMDeviceApp** APIs for license updates and metering data retrieval.</span></span> <span data-ttu-id="bd450-126">Para acessar essa API por meio de WPD, chame **QueryInterface** no **IID \_ IWMDRMDeviceApp** do **IStream** retornado de [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="bd450-126">To access this API through WPD, call **QueryInterface** on **IID\_IWMDRMDeviceApp** from the **IStream** returned from [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="bd450-127">Essa instância do **IWMDRMDeviceApp** está vinculada à conexão do **IPortableDevice** ao seu dispositivo compatível com WMDRM e não ao conteúdo específico em que o **IStream** foi obtido.</span><span class="sxs-lookup"><span data-stu-id="bd450-127">This **IWMDRMDeviceApp** instance tied to the **IPortableDevice** connection to your WMDRM-compatible device, and not the specific content where the **IStream** was obtained.</span></span> <span data-ttu-id="bd450-128">O WPD internamente encapsula as APIs de medição e as torna acessíveis ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd450-128">WPD internally wraps the metering APIs and makes it accessible to your application.</span></span> <span data-ttu-id="bd450-129">Seu aplicativo deve usar a \_ constante de PTR de dispositivo WMDRMDEVICEAPP use \_ WPD \_ \_ para o parâmetro *IWMDMDevice* \* .</span><span class="sxs-lookup"><span data-stu-id="bd450-129">Your application should use the WMDRMDEVICEAPP\_USE\_WPD\_DEVICE\_PTR constant for the *IWMDMDevice*\* parameter.</span></span>

<span data-ttu-id="bd450-130">O trecho de código a seguir demonstra isso.</span><span class="sxs-lookup"><span data-stu-id="bd450-130">The following code snippet demonstrates this.</span></span>


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



<span data-ttu-id="bd450-131">O mesmo pré-requisito com a chave privada do aplicativo e o certificado também se aplica aqui.</span><span class="sxs-lookup"><span data-stu-id="bd450-131">The same pre-requisite with the application private key and certificate applies here as well.</span></span> <span data-ttu-id="bd450-132">Se a chave/certificado for inválido ou se o sistema WMDRM falhar ao ser inicializado, a chamada **QueryInferface** falhará.</span><span class="sxs-lookup"><span data-stu-id="bd450-132">If the key/certificate is invalid or if the WMDRM system fails to initialize, the **QueryInferface** call will fail.</span></span>

<span data-ttu-id="bd450-133">O método acima para adquirir a interface **IWMDRMDeviceApp** do ponteiro **IStream** é apenas uma conveniência se seu aplicativo já estiver fazendo uma transferência de conteúdo protegido anteriormente, antes de prosseguir com as operações de medição e sincronização de licenças.</span><span class="sxs-lookup"><span data-stu-id="bd450-133">The above method to acquire the **IWMDRMDeviceApp** interface from the **IStream** pointer is just a convenience if your application is already doing a prior protected content transfer, before proceeding on to do metering and license synchronization operations.</span></span>

<span data-ttu-id="bd450-134">Nossa recomendação para a maioria dos aplicativos que precisam acessar o **IWMDRMDeviceApp** é inicializar o **IWMDRMDeviceApp** diretamente, pois isso não exige que seu aplicativo transfira o conteúdo protegido ou mantenha as interfaces de transferência para realizar a medição de dispositivos e a sincronização de licenças. Esse método exigirá o uso de APIs do Windows Media Gerenciador de Dispositivos (WMDM).</span><span class="sxs-lookup"><span data-stu-id="bd450-134">Our recommendation for most applications that need to access **IWMDRMDeviceApp** is to initialize **IWMDRMDeviceApp** directly as this does not require your application to transfer protected content or hold on to the transfer interfaces in order to do device metering and license sync. This method will require usage of Windows Media Device Manager (WMDM) APIs.</span></span> <span data-ttu-id="bd450-135">Para obter detalhes e código de exemplo, consulte o White Paper [acessando APIs WMDRM de um aplicativo WPD](../windows-portable-devices.md) no site do whdc.</span><span class="sxs-lookup"><span data-stu-id="bd450-135">For details and sample code, refer to the [Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) whitepaper on the WHDC site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd450-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd450-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd450-137">**Dispositivos portáteis do Windows**</span><span class="sxs-lookup"><span data-stu-id="bd450-137">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
