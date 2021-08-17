---
title: Apresentação
description: A apresentação é a etapa final do processo UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92f8457a881dc0414713e996d230261330c10911f2aea285a2e365ad0d59320
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137189"
---
# <a name="presentation"></a>Apresentação

A apresentação é a etapa final do processo UPnP. Se um dispositivo tiver uma URL para apresentação, um ponto de controle poderá recuperar uma página dessa URL e carregar a página em um navegador. Dependendo dos recursos da página de apresentação e do dispositivo, o ponto de controle pode controlar o dispositivo e exibir o status do dispositivo.

O caminho do recurso, que é passado para [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) durante o registro, é onde todos os arquivos relevantes para a apresentação do dispositivo estão localizados. Os desenvolvedores de dispositivos podem fornecer páginas separadas para cada dispositivo inserido. A URL de apresentação no modelo de descrição do dispositivo pode ser uma URL absoluta ou uma URL relativa. Para URLs relativas, que são relativas ao caminho do recurso, o modelo de descrição do dispositivo deve conter um nome de arquivo. **IUPnPRegistrar** converte isso em uma URL com o local real. Para URLs absolutas, o local não é modificado.

Para dar suporte a scripts do lado do cliente em uma página de apresentação, informações extras normalmente são anexadas à URL na forma de uma "cadeia de caracteres de consulta". As informações extras acrescentadas são a URL para o documento de descrição do dispositivo e o UDN do dispositivo ou dispositivo inserido. A URL de descrição do dispositivo pode ser usada para carregar um documento de descrição no script e, em seguida, controlar o dispositivo por meio de seus serviços. O UDN é usado para selecionar um dispositivo inserido do dispositivo raiz.

O formato da URL de apresentação modificada é: a URL de apresentação real, um ponto de interrogação ("?"), a URL de descrição do dispositivo, um sinal de adição ("+"), o dispositivo UDN. O ponto de interrogação denota o início da cadeia de caracteres de consulta.

Se a URL de apresentação no modelo de descrição do dispositivo era uma URL absoluta e já continha um ponto de interrogação ("?"), as informações extras não são adicionadas à URL da apresentação.



| Descrição                        | URL                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| No modelo de descrição do dispositivo | **presentationURL** MyDevice.html **/presentationURL**                                                                                              |
| Gerado pelo host do dispositivo       | **presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ... + UDN **/presentationURL** |



 

Um script do lado do cliente pode ter que extrair a URL de descrição do dispositivo da URL de apresentação para carregar o objeto [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . Isso é feito por meio da cadeia de caracteres de consulta e de seu encerramento no sinal de adição ("+").


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



No caso de uma página de apresentação para um dispositivo inserido, é necessário algum trabalho adicional. Depois de carregar o [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), o script deve obter a coleção de dispositivos inseridos e, em seguida, selecionar o dispositivo que corresponde ao UDN na cadeia de caracteres de consulta. O script a seguir mostra como selecionar o dispositivo inserido para a página de apresentação atual. Ele pressupõe que LightDesc já está carregado.


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




