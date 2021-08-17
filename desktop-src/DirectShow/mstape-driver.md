---
description: Driver MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Driver MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23eaf6dd7f0d6713b0db5ba5ed21ba4f7640c1373f23cb0066b0b31f366809cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952205"
---
# <a name="mstape-driver"></a>Driver MSTape

este tópico aplica-se ao Windows XP ou posterior.

O driver MSTape dá suporte a dispositivos de camcorder D-VHS e MPEG. Ele é exposto a aplicativos como o filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) . Sua funcionalidade é semelhante à do [MSDV](msdv-driver.md), o driver DV Camcorder:

-   Ele aparece nas categorias de filtro "fontes de captura de vídeo" (CLSID \_ VideoInputDeviceCategory) e "dispositivos de renderização de streaming WDM" (am \_ KSCATEGORY \_ render).
-   Um aplicativo pode criar uma instância do filtro usando a interface [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .
-   Ele tem um pino de saída para captura e transporte do dispositivo e um PIN de entrada para transporte para o dispositivo. Somente um PIN pode ser conectado no momento.

**Tipos de mídia**

O PIN de entrada dá suporte a um tipo de mídia.



| Rótulo | Valor |
|--------------|------------------------------------------------------------|
| Tipo principal   | Fluxo de MEDIATYPE \_                                          |
| Subtype      | \_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_                     |
| Tamanho da Amostra  | 192 x 256                                                  |
| Bloco de formato | [**\_Stride de transporte MPEG2 \_**](mpeg2-transport-stride.md) |



 

O pino de saída dá suporte a dois tipos de mídia.



| Rótulo | Valor |
|--------------|----------------------------------------|
| Tipo principal   | Fluxo de MEDIATYPE \_                      |
| Subtype      | \_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_ |
| Tamanho da Amostra  | 192 x 256                              |
| Bloco de formato | \_Stride de transporte MPEG2 \_               |



 



| Rótulo | Valor |
|--------------|----------------------------------------|
| Tipo principal   | Fluxo de MEDIATYPE \_                      |
| Subtype      | \_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_ |
| Tamanho da Amostra  | 188 x 256                              |
| Bloco de formato | **NULL**                               |



 

**Informações do dispositivo**

O driver lê dinamicamente as informações da ROM de configuração do dispositivo. O aplicativo pode recuperar essas informações ligando o moniker do dispositivo a um recipiente de propriedades e chamando o método **IPropertyBag:: Read** .



| Propriedade            | Descrição                                                                                                                                                                         | Tipo de dados           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueID \_ baixo       | ID exclusiva do dispositivo ( **DWORD** insuficiente).                                                                                                                                            | **Long** (VT \_ i4)   |
| UniqueID \_ alto      | ID exclusiva do dispositivo (alta **DWORD**)                                                                                                                                            | **longo**            |
| VendorID            | ID do fornecedor.                                                                                                                                                                          | **longo**            |
| ModelID             | ID do modelo.                                                                                                                                                                           | **longo**            |
| VendorText          | Nome do fornecedor.                                                                                                                                                                        | **BSTR** (VT \_ BSTR) |
| ModelText           | Nome do modelo do dispositivo.                                                                                                                                                                  | **BSTR**            |
| UnitModelText       | Nome do modelo de unidade; pode ser o mesmo que ModelText.                                                                                                                                      | **BSTR**            |
| DeviceOPcr0Payload  | carga de oPCR (controle de plugue de saída). Exemplo: 146 quadlets.                                                                                                                          | **longo**            |
| DeviceOPcr0DataRate | taxa de dados de oPCR. Exemplos: 0 (S100), 1 (S200) ou 2 (s400).                                                                                                                          | **longo**            |
| DeviceClassGUID     | GUID que identifica o driver de dispositivo. Para MSTape, esse valor é `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` . Esse GUID é definido como MSTapeDeviceGUID no arquivo de cabeçalho Xprtdefs. h. | **BSTR**            |
| Descrição         | Uma descrição do dispositivo, extraída do arquivo INF. Essa cadeia de caracteres geralmente contém o nome da marca do dispositivo.                                                                    | **BSTR**            |



 

A ID do dispositivo é um inteiro de 64 bits. O **DWORD** baixo é armazenado na Propriedade UniqueId \_ Low e o **DWORD** alto é armazenado na \_ Propriedade alta UniqueId.

Para obter mais informações sobre monikers de dispositivo, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Filter](directshow-filters.md)
</dt> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



