---
title: Usando a extensão ADSI para Serviços de Área de Trabalho Remota configuração de usuário
description: A administração de propriedades de usuário específicas de Serviços de Área de Trabalho Remota é possível usando os métodos implementados pela extensão ADSI (Active Directory Service Interfaces), que é empacotada com a biblioteca de vínculo dinâmico Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando a extensão ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917609"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a><span data-ttu-id="a8555-104">Usando a extensão ADSI para Serviços de Área de Trabalho Remota configuração de usuário</span><span class="sxs-lookup"><span data-stu-id="a8555-104">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>

<span data-ttu-id="a8555-105">A extensão de interface de serviço de Active Directory (ADSI) para Serviços de Área de Trabalho Remota configuração de usuário é uma biblioteca que é empacotada com a biblioteca de vínculo dinâmico Tsuserex.dll.</span><span class="sxs-lookup"><span data-stu-id="a8555-105">The Active Directory Service Interfaces (ADSI) extension for Remote Desktop Services user configuration is a library that is packaged with the dynamic-link library Tsuserex.dll.</span></span> <span data-ttu-id="a8555-106">A administração de propriedades de usuário específicas do Serviços de Área de Trabalho Remota é possível usando os métodos implementados pela extensão.</span><span class="sxs-lookup"><span data-stu-id="a8555-106">Administration of Remote Desktop Services-specific user properties is possible using the methods implemented by the extension.</span></span> <span data-ttu-id="a8555-107">Os métodos permitem a configuração das propriedades que estão disponíveis na interface de extensão para usuários Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="a8555-107">The methods allow configuration of the properties that are available in the extension interface for Remote Desktop Services users.</span></span>

<span data-ttu-id="a8555-108">A extensão ADSI para Serviços de Área de Trabalho Remota configuração de usuário dá suporte ao exame e à manipulação de Serviços de Área de Trabalho Remota Propriedades de usuário armazenadas no banco de dados do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="a8555-108">The ADSI extension for Remote Desktop Services user configuration supports the examination and manipulation of Remote Desktop Services user properties stored in the Directory Service database.</span></span> <span data-ttu-id="a8555-109">A extensão também dá suporte à configuração de propriedades do usuário que são armazenadas no Active Directory, por meio da API do protocolo LDAP.</span><span class="sxs-lookup"><span data-stu-id="a8555-109">The extension also supports configuration of user properties that are stored in the Active Directory, through the Lightweight Directory Access Protocol (LDAP) API.</span></span>

<span data-ttu-id="a8555-110">O provedor implementa os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="a8555-110">The provider implements the following methods:</span></span>

-   <span data-ttu-id="a8555-111">[**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span><span class="sxs-lookup"><span data-stu-id="a8555-111">[**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get).</span></span> <span data-ttu-id="a8555-112">Esse método procura uma propriedade específica ou um conjunto de propriedades em uma instância da classe.</span><span class="sxs-lookup"><span data-stu-id="a8555-112">This method searches for a specific property or set of properties on an instance of the class.</span></span>
-   <span data-ttu-id="a8555-113">[**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="a8555-113">[**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put).</span></span> <span data-ttu-id="a8555-114">Esse método configura uma propriedade específica ou um conjunto de propriedades em uma instância da classe.</span><span class="sxs-lookup"><span data-stu-id="a8555-114">This method configures a specific property or set of properties on an instance of the class.</span></span>

<span data-ttu-id="a8555-115">Consulte a [referência para a extensão ADSI para serviços de área de trabalho remota configuração de usuário](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) para obter uma lista das propriedades específicas do usuário serviços de área de trabalho remota que você pode configurar.</span><span class="sxs-lookup"><span data-stu-id="a8555-115">See the [Reference for the ADSI Extension for Remote Desktop Services User Configuration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) for a list of the specific Remote Desktop Services user properties you can configure.</span></span>

<span data-ttu-id="a8555-116">Para obter mais informações sobre como acessar e modificar atributos com ADSI, consulte [acessando e manipulando dados com ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span><span class="sxs-lookup"><span data-stu-id="a8555-116">For more information about accessing and modifying attributes with ADSI, see [Accessing and Manipulating Data with ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).</span></span>

<span data-ttu-id="a8555-117">Para obter mais informações sobre como usar as convenções de nomenclatura ADSI e as cadeias de caracteres de AdsPath, consulte as informações sobre [provedores de serviço ADSI](/windows/desktop/ADSI/adsi-system-providers) individuais na documentação do SDK (Software Development Kit) do [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform.</span><span class="sxs-lookup"><span data-stu-id="a8555-117">For more information about using ADSI naming conventions and AdsPath strings, see the information about individual [ADSI Service Providers](/windows/desktop/ADSI/adsi-system-providers) in the [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK) documentation.</span></span>

 

 