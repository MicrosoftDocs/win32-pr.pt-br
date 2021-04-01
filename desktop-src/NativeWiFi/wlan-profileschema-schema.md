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
# <a name="wlan_profile-schema"></a><span data-ttu-id="22732-103">\_Esquema de perfil WLAN</span><span class="sxs-lookup"><span data-stu-id="22732-103">WLAN\_profile Schema</span></span>

<span data-ttu-id="22732-104">O \_ esquema de perfil WLAN define um perfil de WLAN usado pelo serviço de configuração automática WiFi nativo.</span><span class="sxs-lookup"><span data-stu-id="22732-104">The WLAN\_profile Schema defines a WLAN profile used by the Native Wifi AutoConfig service.</span></span>

<span data-ttu-id="22732-105">O serviço AutoConfig aceita perfis sem fio do agente de Política de Grupo, da interface de script (**netsh**), da interface do usuário ou da interface de configuração do USB Flash.</span><span class="sxs-lookup"><span data-stu-id="22732-105">The AutoConfig service accepts wireless profiles from the Group Policy Agent, the scripting interface (**netsh**), the user interface, or from the USB flash configuration interface.</span></span>

<span data-ttu-id="22732-106">Um perfil recebido de um desses sistemas é mapeado para o esquema de \_ perfil de WLAN e armazenado no repositório de perfis.</span><span class="sxs-lookup"><span data-stu-id="22732-106">A profile received from one of these systems is mapped to the WLAN\_profile schema and stored in the profile store.</span></span> <span data-ttu-id="22732-107">Os perfis podem ser exportados do repositório de perfis usando comandos netsh ou usando elementos de API, como [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span><span class="sxs-lookup"><span data-stu-id="22732-107">Profiles can be exported from the profile store using netsh commands or using API elements such as [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span></span>

<span data-ttu-id="22732-108">O elemento raiz de um perfil de WLAN é o elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="22732-108">The root element of a WLAN profile is the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span> <span data-ttu-id="22732-109">Cada perfil terá exatamente um elemento raiz.</span><span class="sxs-lookup"><span data-stu-id="22732-109">Each profile will have exactly one root element.</span></span> <span data-ttu-id="22732-110">O elemento **WLANProfile** está no namespace `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="22732-110">The **WLANProfile** element is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

<span data-ttu-id="22732-111">Para exibir os perfis de WLAN de exemplo, consulte [exemplos de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="22732-111">To view sample WLAN profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

-   [<span data-ttu-id="22732-112">\_Elementos do esquema do perfil WLAN</span><span class="sxs-lookup"><span data-stu-id="22732-112">WLAN\_profile Schema Elements</span></span>](wlan-profileschema-elements.md)
-   [<span data-ttu-id="22732-113">\_Tipos simples de esquema de perfil WLAN</span><span class="sxs-lookup"><span data-stu-id="22732-113">WLAN\_profile Schema Simple Types</span></span>](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a><span data-ttu-id="22732-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22732-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="22732-115">[Comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="22732-115">[Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span></span>
</dt> </dl>

 

 
