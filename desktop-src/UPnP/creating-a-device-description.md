---
title: Criando uma descrição de dispositivo
description: Uma descrição de dispositivo baseada em UPnP é um documento XML que descreve as propriedades de um dispositivo e a hierarquia de dispositivos aninhados dentro dele.
ms.assetid: b2a7d342-958c-439d-8b17-b4fdc5fbad12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52df95de15481c7004704b6f67cd9478083ac88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916144"
---
# <a name="creating-a-device-description"></a>Criando uma descrição de dispositivo

Uma [*Descrição de dispositivo*](d-gly.md) baseada em UPnP é um documento XML que descreve as propriedades de um dispositivo e a hierarquia de dispositivos aninhados dentro dele. O esquema para descrições de dispositivos baseadas em UPnP, conhecido como UTL (linguagem de modelo UPnP) para dispositivos, é definido na arquitetura do dispositivo UPnP. As descrições de dispositivo contêm links para [*descrições de serviço*](s-gly.md). O esquema para descrições de serviço e o UTL para serviços também são definidos na especificação "arquitetura de dispositivo UPnP".

> [!Note]  
> Pode haver problemas ao usar a descrição do serviço de www.upnp.org.

 

O desenvolvedor de um dispositivo deve fornecer descrições de dispositivo e serviço para o dispositivo.

Os elementos de uma descrição de dispositivo que o desenvolvedor de um dispositivo hospedado deve fornecer são os mesmos definidos na especificação "arquitetura de dispositivo UPnP", com as seguintes exceções:

-   Os elementos **controlURL** e **eventSubURL** são obrigatórios e devem estar vazios. O host do dispositivo preenche valores para esses campos quando o dispositivo é publicado e anunciado.
-   O elemento **UDN** deve conter um identificador exclusivo para o documento de descrição do dispositivo (ou seja, ele não precisa ser globalmente exclusivo). Esse identificador é usado para pesquisar o UDN gerado pelo host do dispositivo.
-   Os elementos **SCPDURL** não devem conter URLs para descrições de serviço. Em vez disso, eles devem conter o nome do arquivo de descrição do serviço. O arquivo de descrição do serviço deve estar localizado no [*diretório de recursos*](r-gly.md). O local desse diretório deve ser fornecido ao host do dispositivo durante o processo de registro, como o uso de um programa de instalação. Esse caminho e todos abaixo são caminhos relativos, com base no caminho registrado.
-   O elemento **URL** dentro do elemento **Icon** não deve conter URLs para ícones de dispositivo. Em vez disso, eles devem conter o nome do arquivo de ícone. Se presente, o arquivo de ícone deve estar localizado no diretório de recursos. Esse caminho e todos abaixo são caminhos relativos, com base no caminho registrado.
-   O elemento **URLbase** não deve estar presente.

> [!Note]  
> Todas as URLs geradas pelo host do dispositivo são URLs relativas. As URLs são relativas ao local do documento de descrição do dispositivo, que é enviado no anúncio inicial do dispositivo.

 

> [!IMPORTANT]
> Não adicione comentários ao documento de descrição do dispositivo, pois isso pode causar falhas de registro quando o host do dispositivo Universal Plug and Play tentar analisar o documento.

 

## <a name="string-length-limitations"></a>Limitações de comprimento da cadeia de caracteres

Os seguintes comprimentos de cadeia de caracteres são usados na API de host do dispositivo com tecnologia UPnP:

-   **DeviceType** – 64 bytes
-   **FriendlyName** – 64 bytes
-   **fabricante** – 64 bytes
-   **ModelDescription** – 128 bytes
-   **ModelName** – 32 bytes
-   **modelNumber** – 32 bytes
-   **SerialNumber** – 64 bytes
-   **UPC** – 12 bytes
-   **ServiceType** – 64 bytes
-   **ServiceId** – 64 bytes

 

 




