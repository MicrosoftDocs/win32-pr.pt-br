---
description: Define um perfil de WLAN usado pelo serviço de configuração automática WiFi nativo.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Esquema de WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090216"
---
# <a name="wlan_profile-schema"></a>\_Esquema de perfil WLAN

O \_ esquema de perfil WLAN define um perfil de WLAN usado pelo serviço de configuração automática WiFi nativo.

O serviço AutoConfig aceita perfis sem fio do agente de Política de Grupo, da interface de script (**netsh**), da interface do usuário ou da interface de configuração do USB Flash.

Um perfil recebido de um desses sistemas é mapeado para o esquema de \_ perfil de WLAN e armazenado no repositório de perfis. Os perfis podem ser exportados do repositório de perfis usando comandos netsh ou usando elementos de API, como [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).

O elemento raiz de um perfil de WLAN é o elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) . Cada perfil terá exatamente um elemento raiz. O elemento **WLANProfile** está no namespace `https://www.microsoft.com/networking/WLAN/profile/v1` .

Para exibir os perfis de WLAN de exemplo, consulte [exemplos de perfil sem fio](wireless-profile-samples.md).

-   [\_Elementos do esquema do perfil WLAN](wlan-profileschema-elements.md)
-   [\_Tipos simples de esquema de perfil WLAN](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))
</dt> </dl>

 

 
