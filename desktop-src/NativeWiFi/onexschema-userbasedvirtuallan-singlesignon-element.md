---
description: Especifica se a LAN virtual (VLAN) usada pelo dispositivo é alterada com base nas credenciais do usuário.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Elemento userBasedVirtualLan (logon único)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090662"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a><span data-ttu-id="e6020-103">Elemento userBasedVirtualLan (logon único)</span><span class="sxs-lookup"><span data-stu-id="e6020-103">userBasedVirtualLan (singleSignOn) Element</span></span>

<span data-ttu-id="e6020-104">O elemento userBasedVirtualLan (logon único) especifica se a LAN virtual (VLAN) usada pelo dispositivo é alterada com base nas credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="e6020-104">The userBasedVirtualLan (singleSignOn) element specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="e6020-105">Alguns dispositivos de NAS (servidor de acesso à rede) alteram a VLAN após a autenticação de um usuário.</span><span class="sxs-lookup"><span data-stu-id="e6020-105">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="e6020-106">Quando userBasedVirtualLan for TRUE, o NAS poderá alterar a VLAN de um dispositivo após a autenticação de um usuário.</span><span class="sxs-lookup"><span data-stu-id="e6020-106">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span>

<span data-ttu-id="e6020-107">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="e6020-107">This element is optional.</span></span> <span data-ttu-id="e6020-108">Quando userBasedVirtualLan não é especificado em um perfil, um valor de FALSE é usado.</span><span class="sxs-lookup"><span data-stu-id="e6020-108">When userBasedVirtualLan is not specified in a profile, a value of FALSE is used.</span></span>

<span data-ttu-id="e6020-109">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="e6020-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="e6020-110">O elemento **userBasedVirtualLan** é definido pelo elemento [**logon único**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e6020-110">The **userBasedVirtualLan** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6020-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6020-111">Remarks</span></span>

<span data-ttu-id="e6020-112">Esse parâmetro pode ser definido na linha de comando usando o comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="e6020-112">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="e6020-113">Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="e6020-113">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6020-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6020-114">Requirements</span></span>



| <span data-ttu-id="e6020-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6020-115">Requirement</span></span> | <span data-ttu-id="e6020-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e6020-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6020-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6020-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e6020-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6020-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6020-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6020-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e6020-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6020-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6020-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6020-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6020-122">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="e6020-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e6020-123">**Logon único**</span><span class="sxs-lookup"><span data-stu-id="e6020-123">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="e6020-124">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="e6020-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e6020-125">**Logon único (OneX)**</span><span class="sxs-lookup"><span data-stu-id="e6020-125">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
