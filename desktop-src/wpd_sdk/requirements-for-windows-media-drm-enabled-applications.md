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
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Requisitos para aplicativos do Windows Media DRM-Enabled

Para criar um aplicativo habilitado para Windows Media Digital Rights Management (DRM), você deve ter os cabeçalhos e as bibliotecas descritos na seção [requisitos gerais para o desenvolvimento de aplicativos](general-requirements-for-application-development.md) deste documento. Além disso, o aplicativo precisará fornecer propriedades adicionais nas informações do cliente ao abrir o dispositivo.

As duas propriedades adicionais que são necessárias para habilitar transferências de conteúdo protegidas por DRM do Windows Media são descritas na tabela a seguir.



| Propriedade                                      | Descrição                              |
|-----------------------------------------------|------------------------------------------|
| \_ \_ \_ chave privada do aplicativo \_ de cliente WPD \_ | Especifica a chave privada do aplicativo. |
| \_certificado de \_ aplicativo de WMDRM cliente \_ WPD \_  | Especifica o certificado do aplicativo. |



 

Essas propriedades devem ser fornecidas nas informações do cliente do aplicativo quando o dispositivo for aberto com o método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) . Quando essas propriedades são fornecidas, a API WPD permite transferências de conteúdo protegidas. Se o aplicativo tiver fornecido um certificado e uma chave privada, a API criará um canal seguro para transferir conteúdo WMDRM protegido para o dispositivo.

Para obter informações sobre como criar e distribuir aplicativos baseados no Windows que dão suporte ao Windows Media DRM, consulte o tópico [Licenciamento de aplicativos baseados no Windows](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) a seguir.

## <a name="transferring-content"></a>Transferindo conteúdo

Para transferir conteúdo protegido por WMDRM, use [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Esse método pode ser usado para conteúdo protegido e não criptografado sem opções adicionais. A API WPD selecionará automaticamente o canal protegido ou não criptografado, dependendo se o conteúdo está protegido ou claro. Ele interage com o provedor de conteúdo do WMDRM Secure para processar as licenças WMDRM.

## <a name="transferring-known-clear-content"></a>Transferindo conteúdo de limpeza conhecido

Se você habilitou seu aplicativo para lidar com o conteúdo protegido, mas souber que um arquivo específico não está protegido, você pode informar a WPD para ignorar o processamento de DRM ao definir a opção de **API WPD use a opção de \_ \_ \_ \_ \_ \_ fluxo de dados CLEAR** como true no **IPortableDeviceValues** de entrada ao chamar [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para limpar conteúdo.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Acessando operações de medição usando IWMDRMDeviceApp

O WPD fornece um mecanismo para acessar as APIs do **IWMDRMDeviceApp** para atualizações de licenças e a recuperação de dados de medição. Para acessar essa API por meio de WPD, chame **QueryInterface** no **IID \_ IWMDRMDeviceApp** do **IStream** retornado de [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Essa instância do **IWMDRMDeviceApp** está vinculada à conexão do **IPortableDevice** ao seu dispositivo compatível com WMDRM e não ao conteúdo específico em que o **IStream** foi obtido. O WPD internamente encapsula as APIs de medição e as torna acessíveis ao seu aplicativo. Seu aplicativo deve usar a \_ constante de PTR de dispositivo WMDRMDEVICEAPP use \_ WPD \_ \_ para o parâmetro *IWMDMDevice* \* .

O trecho de código a seguir demonstra isso.


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



O mesmo pré-requisito com a chave privada do aplicativo e o certificado também se aplica aqui. Se a chave/certificado for inválido ou se o sistema WMDRM falhar ao ser inicializado, a chamada **QueryInferface** falhará.

O método acima para adquirir a interface **IWMDRMDeviceApp** do ponteiro **IStream** é apenas uma conveniência se seu aplicativo já estiver fazendo uma transferência de conteúdo protegido anteriormente, antes de prosseguir com as operações de medição e sincronização de licenças.

Nossa recomendação para a maioria dos aplicativos que precisam acessar o **IWMDRMDeviceApp** é inicializar o **IWMDRMDeviceApp** diretamente, pois isso não exige que seu aplicativo transfira o conteúdo protegido ou mantenha as interfaces de transferência para realizar a medição de dispositivos e a sincronização de licenças. Esse método exigirá o uso de APIs do Windows Media Gerenciador de Dispositivos (WMDM). Para obter detalhes e código de exemplo, consulte o White Paper [acessando APIs WMDRM de um aplicativo WPD](../windows-portable-devices.md) no site do whdc.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Dispositivos portáteis do Windows**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
