---
description: Especifica, em segundos, o atraso máximo antes da tentativa de conexão de logon único falhar.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Elemento maxDelay (logon único)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828236"
---
# <a name="maxdelay-singlesignon-element"></a><span data-ttu-id="d9e19-103">Elemento maxDelay (logon único)</span><span class="sxs-lookup"><span data-stu-id="d9e19-103">maxDelay (singleSignOn) Element</span></span>

<span data-ttu-id="d9e19-104">O elemento maxDelay (logon único) especifica, em segundos, o atraso máximo antes da tentativa de conexão de logon único falhar.</span><span class="sxs-lookup"><span data-stu-id="d9e19-104">The maxDelay (singleSignOn) element specifies, in seconds, the maximum delay before the single sign on connection attempt fails.</span></span>

<span data-ttu-id="d9e19-105">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="d9e19-105">This element is optional.</span></span> <span data-ttu-id="d9e19-106">Quando maxDelay não é especificado em um perfil, é usado um valor de 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="d9e19-106">When maxDelay is not specified in a profile, a value of 10 seconds is used.</span></span>

<span data-ttu-id="d9e19-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="d9e19-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxDelay">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="0"
             />
            <xs:enumeration
                value="120"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="d9e19-108">O elemento **maxDelay** é definido pelo elemento [**logon único**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e19-108">The **maxDelay** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e19-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9e19-109">Remarks</span></span>

<span data-ttu-id="d9e19-110">Esse parâmetro pode ser definido na linha de comando usando o comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="d9e19-110">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="d9e19-111">Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d9e19-111">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e19-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9e19-112">Requirements</span></span>



| <span data-ttu-id="d9e19-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9e19-113">Requirement</span></span> | <span data-ttu-id="d9e19-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e19-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d9e19-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9e19-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d9e19-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9e19-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9e19-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9e19-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d9e19-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d9e19-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9e19-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="d9e19-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9e19-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="d9e19-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d9e19-121">**Logon único**</span><span class="sxs-lookup"><span data-stu-id="d9e19-121">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="d9e19-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="d9e19-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d9e19-123">**Logon único (OneX)**</span><span class="sxs-lookup"><span data-stu-id="d9e19-123">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
