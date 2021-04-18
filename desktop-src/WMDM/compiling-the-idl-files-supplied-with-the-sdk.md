---
title: Compilando os arquivos IDL fornecidos com o SDK
description: Compilando os arquivos IDL fornecidos com o SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Windows Media Gerenciador de Dispositivos, arquivos IDL
- Gerenciador de Dispositivos, arquivos IDL
- aplicativos de área de trabalho, arquivos IDL
- provedores de serviço, arquivos IDL
- Guia de programação, arquivos IDL
- arquivos IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105800185"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Compilando os arquivos IDL fornecidos com o SDK

O SDK do Windows Media Gerenciador de Dispositivos inclui os arquivos de cabeçalho e os arquivos IDL de origem para a maioria desses arquivos de cabeçalho. Os arquivos de cabeçalho estão localizados na \\ \\ pasta Inc no caminho de instalação do SDK. Os arquivos IDL estão localizados na \\ pasta IDL \\ .

Os cabeçalhos pré-compilados são muito mais simples de usar e vários arquivos IDL são combinados em um único cabeçalho fornecido. No entanto, se você decidir processar seus próprios arquivos de cabeçalho dos arquivos IDL fornecidos, este tópico descreverá quais arquivos IDL criam quais arquivos de cabeçalho e também descreve as dependências de cada arquivo IDL.

**IDL equivalente e arquivos de cabeçalho fornecidos**



| **INSERI**                                                                                            | **Cabeçalho fornecido equivalente**               | **Descrição**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM. idl<br/> WMSP. idl<br/> WMSCP. idl<br/> icomponentauthenticate. idl<br/> | Mswmdm. h                                     | Todos os quatro arquivos IDL estão incluídos neste cabeçalho único fornecido.<br/> **WMDM. idl** define todas as interfaces de aplicativo e estruturas, constantes e códigos de erro necessários.<br/> **WMSP. idl** define todas as interfaces do provedor de serviços.<br/> **WMSCP. idl** define todas as interfaces, os valores de GUID e as constantes exigidas por provedores de conteúdo seguro.<br/> **icomponentauthenticate. idl** define a interface [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .<br/> |
| Wmdmlog. idl                                                                                        | Wmdmlog. h<br/> wmdmlog \_ i. c<br/> | Define as interfaces de log.<br/> Ambos os arquivos de cabeçalho fornecidos devem ser usados, em vez de apenas o arquivo. h, devido a um problema com o arquivo IDL.<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp. idl                                                                                 | Wmdrmdeviceapp. h                             | Define as interfaces [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) usadas por aplicativos que atualizam DRM em dispositivos ou contagens de planos de execução em dispositivos.                                                                                                                                                                                                                                                                                                                 |



 

**Dependências de IDL**

Vários dos arquivos IDL fornecidos têm dependências de compilação. Se você planeja compilar os arquivos IDL por conta própria, deve processar essas dependências externas na ordem mostrada na tabela a seguir.



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| **INSERI**                    | **Dependências**                                                                 |
| icomponentauthenticate. idl | importe "oaidl. idl";<br/> \#incluir "icomponentauthenticate. idl"<br/> |
| WMDM. idl                   | Nenhuma dependência externa                                                         |
| WmdmLog. idl                | Nenhuma dependência externa                                                         |
| WMDRMDeviceApp. idl         | Nenhuma dependência externa                                                         |
| WMSCP. idl                  | \#incluir "WMDRMDeviceApp. idl"<br/> \#incluir "WMSP. idl"<br/>        |
| WMSP. idl                   | \#incluir "WMDM. idl"                                                             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tarefas comuns a aplicativos e provedores de serviços**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





