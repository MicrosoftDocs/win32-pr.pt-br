---
description: Requisitos para Windows aplicativos DRM-Enabled mídia
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Requisitos para Windows aplicativos DRM-Enabled mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ad59b5b590436ca5734fcb8d226d41f4f995a5d4ea97e0c46d771df476be6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027045"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Requisitos para Windows aplicativos DRM-Enabled mídia

Para criar um aplicativo habilitado para DRM (Windows Media Digital Rights Management), você deve ter os [](general-requirements-for-application-development.md) headers e bibliotecas descritos na seção Requisitos gerais para desenvolvimento de aplicativos deste documento. Além disso, o aplicativo precisará fornecer propriedades adicionais nas informações do cliente ao abrir o dispositivo.

As duas propriedades adicionais necessárias para habilitar Windows transferências de conteúdo protegidas por DRM de mídia são descritas na tabela a seguir.



| Propriedade                                      | Descrição                              |
|-----------------------------------------------|------------------------------------------|
| CHAVE PRIVADA DO APLICATIVO \_ WPD CLIENT \_ WMDRM \_ \_ \_ | Especifica a chave privada do aplicativo. |
| CERTIFICADO DE \_ APLICATIVO \_ WMDRM \_ DO CLIENTE WPD \_  | Especifica o certificado do aplicativo. |



 

Essas propriedades devem ser fornecidas nas informações do cliente do aplicativo quando o dispositivo é aberto com o [**método IPortableDevice::Open.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) Quando essas propriedades são fornecidas, a API WPD permite transferências de conteúdo protegidas. Se o aplicativo tiver fornecido um certificado e uma chave privada, a API criará um canal seguro para transferir o conteúdo protegido do WMDRM para o dispositivo.

Para obter informações sobre como criar e distribuir Windows aplicativos baseados em Windows drm de mídia, consulte o tópico Licenciamento [Windows aplicativos baseados em .](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx)

## <a name="transferring-content"></a>Transferindo conteúdo

Para transferir conteúdo protegido por WMDRM, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Esse método pode ser usado para conteúdo protegido e não protegido sem opções adicionais. A API WPD selecionará automaticamente o canal protegido ou não, dependendo se o conteúdo está protegido ou não. Ele faz interfaces com o Provedor de Conteúdo Seguro WMDRM para processar as licenças do WMDRM.

## <a name="transferring-known-clear-content"></a>Transferindo conteúdo não limpo conhecido

Se você habilitar seu aplicativo para lidar com o conteúdo protegido, mas sabe que um arquivo específico não está protegido, poderá pedir ao WPD para ignorar o processamento de DRM definindo a opção **DE API WPD \_ USE CLEAR DATA \_ \_ \_ \_ \_ STREAM** como TRUE na entrada **IPortableDeviceValues** ao chamar [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para conteúdo não criptografado.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Acessando operações de medição usando IWMDRMDeviceApp

O WPD fornece um mecanismo para acessar as APIs **IWMDRMDeviceApp** para atualizações de licença e recuperação de dados de medição. Para acessar essa API por meio de WPD, chame **QueryInterface** no **\_ IID IWMDRMDeviceApp** do **IStream** retornado de [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Essa **instância IWMDRMDeviceApp** vinculada à conexão **IPortableDevice** ao dispositivo compatível com WMDRM e não ao conteúdo específico em que **o IStream** foi obtido. O WPD envolve internamente as APIs de medição e o torna acessível para seu aplicativo. Seu aplicativo deve usar a constante WMDRMDEVICEAPP USE WPD DEVICE PTR para o parâmetro \_ \_ \_ \_ *IWMDMDevice.* \*

O snippet de código a seguir demonstra isso.


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



O mesmo pré-requisito com a chave privada e o certificado do aplicativo também se aplica aqui. Se a chave/certificado for inválido ou se o sistema WMDRM não for inicializado, a **chamada QueryInferface** falhará.

O método acima para adquirir a interface **IWMDRMDeviceApp** do ponteiro **IStream** é apenas uma conveniência se o aplicativo já estiver fazendo uma transferência de conteúdo protegida anteriormente, antes de continuar a fazer operações de sincronização de licença e medição.

Nossa recomendação para a maioria dos aplicativos que precisam acessar **IWMDRMDeviceApp** é inicializar **IWMDRMDeviceApp** diretamente, pois isso não exige que seu aplicativo transfira conteúdo protegido ou mantenha as interfaces de transferência para fazer a medição do dispositivo e a sincronização de licenças. Esse método exigirá o uso de Windows APIs de Gerenciador de Dispositivos (WMDM). Para obter detalhes e código de exemplo, consulte o whitepaper [Acessando APIs wmDRM](../windows-portable-devices.md) de um aplicativo WPD no site do WHDC.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Dispositivos portáteis**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
