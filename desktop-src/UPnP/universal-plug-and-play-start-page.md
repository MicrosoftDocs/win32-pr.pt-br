---
title: APIs de UPnP
description: A estrutura UPnP permite a rede dinâmica de dispositivos inteligentes, computadores sem fio e PCs.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104084975"
---
# <a name="upnp-apis"></a>APIs de UPnP

## <a name="purpose"></a>Finalidade

A estrutura UPnP permite a rede dinâmica de dispositivos inteligentes, computadores sem fio e PCs. Há duas APIs para trabalhar com dispositivos certificados para UPnP:

-   A API do ponto de controle, que consiste em um conjunto de interfaces COM usadas para localizar e controlar dispositivos.
-   A API de host do dispositivo, que consiste em um conjunto de interfaces COM usadas para implementar dispositivos hospedados por um computador.

## <a name="where-applicable"></a>Quando aplicável

A API do ponto de controle permite que os desenvolvedores gravem aplicativos que pesquisam e controlam dispositivos com certificação UPnP. A API de host do dispositivo permite que os desenvolvedores implementem a funcionalidade de dispositivos certificados por UPnP e usem o host do dispositivo para gerenciar as funções de descoberta, descrição, controle, apresentação e eventos de um dispositivo certificado por UPnP.

## <a name="developer-audience"></a>Público de desenvolvedores

Os desenvolvedores que usam as APIs do ponto de controle e as APIs de host do dispositivo devem estar familiarizados com a arquitetura do dispositivo UPnP. Para obter mais informações, consulte a [documentação de implementação de UPnP](https://openconnectivity.org/resources/upnpresources.zip) e o [Fórum UPnP](https://openconnectivity.org/).

Os desenvolvedores que estão usando as APIs de host do dispositivo devem estar familiarizados com as interfaces de Active Template Library (ATL) e COM.

As APIs do ponto de controle e as APIs de host do dispositivo são usadas por uma variedade de aplicativos, desde scripts inseridos em páginas HTML até programas completos de C++ e Microsoft Visual Basic.

Somente a API do ponto de controle dá suporte a Visual Basic Scripting Edition (VBScript).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

A API do ponto de controle é usada em computadores que executam o Microsoft Windows Millennium Edition, o Windows XP, o Windows XP Professional e o Windows CE .NET.

A API de host do dispositivo é usada em computadores que executam o Windows XP, o Windows XP Professional e o Windows CE .NET.

Para obter informações mais específicas sobre quais sistemas operacionais dão suporte a uma função específica, consulte "requisitos" na documentação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                          | Descrição                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Visão geral da arquitetura UPnP](overview-of-universal-plug-and-play.md)<br/>            | Informações gerais e plano de fundo.<br/>                                                     |
| [Visão geral do ponto de controle](control-point-api.md)<br/>                                     | Informações gerais sobre a API do ponto de controle.<br/>                                        |
| [Usando a API do ponto de controle](using-the-control-point-api-with-upnp-technology.md)<br/> | Código de exemplo que mostra como desenvolver aplicativos que controlam dispositivos certificados por UPnP.<br/> |
| [Referência de API de ponto de controle](control-point-api-with-upnp-technology-reference.md)<br/> | Documentação de interfaces de componente de ponto de controle, métodos e eventos.<br/>               |
| [Visão geral da API de host do dispositivo](device-host-api.md)<br/>                                     | Informações gerais sobre a API de host do dispositivo.<br/>                                          |
| [Usando a API de host do dispositivo](using-the-device-host-api-with-upnp-technology.md)<br/>     | Código de exemplo que mostra como desenvolver um aplicativo para dispositivos certificados por UPnP.<br/>        |
| [Referência da API do host do dispositivo](device-host-api-with-upnp-technology-reference.md)<br/>     | Documentação de interfaces, métodos e eventos do componente de host do dispositivo.<br/>                 |



 

 

 





