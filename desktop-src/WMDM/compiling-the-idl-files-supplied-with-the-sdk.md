---
title: Compilando os arquivos IDL fornecidos com o SDK
description: Compilando os arquivos IDL fornecidos com o SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Arquivos de Gerenciador de Dispositivos,IDL
- Gerenciador de Dispositivos, arquivos IDL
- aplicativos da área de trabalho, arquivos IDL
- provedores de serviços, arquivos IDL
- guia de programação, arquivos IDL
- arquivos IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89ae614d6e20d0b05d9b7b6f054505433f4a4d33e2f9feaff60a37f7605e9ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586335"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Compilando os arquivos IDL fornecidos com o SDK

O Windows media Gerenciador de Dispositivos SDK inclui arquivos de header e os arquivos IDL de origem para a maioria desses arquivos de header. Os arquivos de header estão localizados na \\ pasta inc no caminho de instalação do \\ SDK. Os arquivos IDL estão localizados na \\ pasta \\ idl.

Os headers pré-compilados são muito mais simples de usar e vários dos arquivos IDL são combinados em um único header fornecido. No entanto, se você decidir processar seus próprios arquivos de header dos arquivos IDL fornecidos, este tópico descreverá quais arquivos IDL criarão quais arquivos de título e também descreverão as dependências de cada arquivo IDL.

**IDL equivalente e arquivos de header fornecidos**



| **Idl**                                                                                            | **Header fornecido equivalente**               | **Descrição**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM.idl<br/> WMSP.idl<br/> WMSCP.idl<br/> icomponentauthenticate.idl<br/> | Mswmdm.h                                     | Todos os quatro arquivos IDL estão incluídos neste único header fornecido.<br/> **WMDM.idl** Define todas as interfaces de aplicativo e estruturas, constantes e códigos de erro necessários.<br/> **WMSP.idl** Define todas as interfaces do provedor de serviços.<br/> **WMSCP.idl** Define todas as interfaces, valores de GUID e constantes exigidas por provedores de conteúdo seguros.<br/> **icomponentauthenticate.idl** Define a interface [**IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)<br/> |
| Wmdmlog.idl                                                                                        | Wmdmlog.h<br/> wmdmlog \_ i.c<br/> | Define as interfaces de log.<br/> Ambos os arquivos de header fornecidos devem ser usados, em vez de apenas o arquivo .h, devido a um problema com o arquivo IDL.<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp.idl                                                                                 | Wmdrmdeviceapp.h                             | Define as interfaces [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) usadas por aplicativos que atualizam o DRM em dispositivos ou contagens de reprodução de medidor nos dispositivos.                                                                                                                                                                                                                                                                                                                 |



 

**Dependências de IDL**

Vários dos arquivos IDL fornecidos têm dependências de build. Se você planeja compilar os arquivos IDL por conta própria, deverá processar essas dependências externas na ordem mostrada na tabela a seguir.



|   Idl                      |   Dependências                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| icomponentauthenticate.idl | importar "o o adl.idl";<br/> \#incluir "icomponentauthenticate.idl"<br/> |
| WMDM.idl                   | Nenhuma dependência externa                                                         |
| WmdmLog.idl                | Nenhuma dependência externa                                                         |
| WMDRMDeviceApp.idl         | Nenhuma dependência externa                                                         |
| WMSCP.idl                  | \#incluir "WMDRMDeviceApp.idl"<br/> \#incluir "WMSP.idl"<br/>        |
| WMSP.idl                   | \#incluem "WMDM.idl"                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tarefas comuns a aplicativos e provedores de serviços**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





